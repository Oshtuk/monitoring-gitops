# 🚀 Monitoring GitOps Stack for Rails App

📌 **Автор:** [@Oshtuk](https://github.com/Oshtuk)  
📦 **Цель:** Развёртывание приложения на Rails в Kubernetes с мониторингом и GitOps через ArgoCD  
🌐 **Репозиторий:** [github.com/Oshtuk/monitoring-gitops](https://github.com/Oshtuk/monitoring-gitops)

---

## 🔧 Стек технологий

| Компонент        | Назначение                                   |
|------------------|-----------------------------------------------|
| **Kubernetes**   | Платформа оркестрации                        |
| **ArgoCD**       | GitOps для автоматической синхронизации      |
| **Helm**         | Пакетный менеджер для K8s приложений         |
| **Grafana**      | Визуализация метрик                          |
| **VictoriaMetrics** | Хранение и сбор метрик                    |
| **Fluent Bit**   | Сбор и пересылка логов                       |
| **Rails**        | Основное приложение                          |

---

## 📂 Структура репозитория

```text
.
├── argo-apps/            # ArgoCD приложения
│   └── rails-app.yaml    # Application CRD для Rails
├── charts/               # Helm-чарты
│   ├── rails-app/        # Helm-чарт для Rails
│   ├── grafana/
│   ├── fluent-bit/
│   └── ...
├── apps/                 # Kustomize директории
│   └── rails-app/
│       ├── deployment.yaml
│       ├── service.yaml
│       └── kustomization.yaml
└── README.md             # Этот файл
