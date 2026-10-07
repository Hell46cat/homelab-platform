# homelab-platform

Deployment-репозиторий для хоста/виртуальных машин Proxmox VE (mini-PC GMKtec M5 Plus): production Docker Compose, Ansible плейбуки, операционные скрипты и эксплуатационные runbooks.

- **База знаний и архитектура**: [homelab-wiki](../homelab-wiki/home-lab/docs/00-index.md).
- **Исходный код приложений**: [homelab-apps](../homelab-apps/README.md).

---

## Структура

```text
homelab-platform/
├── compose/       # Production Compose stacks и сервисы (Uptime Kuma, Nginx и т.д.)
├── ansible/       # Повторяемая настройка хоста и VM
├── scripts/       # Скрипты деплоя, верификации, бэкапа и восстановления
├── docs/          # Эксплуатационные runbooks (инструкции обслуживания)
├── .env.example   # Шаблон переменных окружения
└── README.md
```

---

## Пути на сервере (Debian VM `vm-core`)

```text
/opt/homelab-platform/      # Git checkout этого репозитория
/srv/homelab/<service>/     # Постоянные данные контейнеров (volumes)
/etc/homelab/<service>.env  # Секреты и хост-специфичные переменные
```

---

## Правила безопасности

- Секреты, боевые `.env`, приватные SSH/TLS ключи, дампы БД и бэкапы **никогда не коммитятся в Git**.
- Сервисы добавляются по одному после локальной проверки и описания health check, update, rollback и restore.
- Подробный регламент выкладки: [20-development-and-deploy.md](../homelab-wiki/home-lab/docs/20-development-and-deploy.md).
