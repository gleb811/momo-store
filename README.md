Пельменная
Репозиторий для хранения кода приложения, из которого собираются два контейнера momo-backend и momo-frontend Приложение доступно по адресу http://momo-store.glebfedotov.ru/

Сборка
Сборка реализована через gitlab CI. Сам build происходит через kaniko с кэшированием. Тестирование кода выполнено через sonarqube Для go дополнительно выполняются unittest

Deploy
Приложение деплоится в K8S кластер, который развернут в Yandex.Cloud с использованием Managed Kubernetes. Continuous Deployment реализован через ArgoCD, который поднимается в кластере K8S. При создании merge request в branch, ArgoCD создаст Review App что позволит проверить работоспособность приложния.

Инфраструктура
https://gitlab.praktikum-services.ru/std-024-07/momo-store-infrastructure

Helm
https://gitlab.praktikum-services.ru/std-024-07/momo-store-helm
```
