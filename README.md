# homelab-platform

Отдельный deployment-репозиторий mini-PC: production Docker Compose, Ansible, операционные scripts, сетевые конфиги без секретов и runbooks.

Причины решений и учебные объяснения находятся в `personal-it/home-lab/docs`. Исходный код приложений — в отдельных репозиториях `personal-it/apps/<service-name>`.

## Структура

```text
homelab-platform/
├── compose/       production stacks и сервисы
├── ansible/       повторяемая настройка хоста
├── network/       безопасные конфиги сетевых устройств
├── scripts/       deploy, verification, backup и restore helpers
├── docs/          только эксплуатационные runbooks
├── .env.example
└── README.md
```

## Пути на сервере

```text
/opt/homelab-platform/      этот Git checkout
/srv/homelab/<service>/     постоянные данные
/etc/homelab/<service>.env  секреты и machine-specific настройки
```

Секреты, реальные `.env`, private keys, database files, firmware и сырые backups не коммитятся.

Сервисы добавляются по одному после ручной проверки, описания health check, update, rollback и restore.

Полный процесс: `personal-it/home-lab/docs/development-and-deployment.md`.
