# OpenWrt configuration

Version-controlled конфигурация OpenWrt без секретов.

Для подтверждённого устройства создаётся каталог `network/openwrt/<device-name>/`:

```text
<device-name>/
├── index.md       модель, revision, роль и способ восстановления
├── config/        sanitized конфигурация без credentials
├── files/         overlay-файлы для контролируемого развёртывания
└── scripts/       проверяемые idempotent helpers
```

Не коммитить:

- полный backup роутера;
- Wi-Fi passwords;
- WireGuard/OpenVPN private keys;
- токены DDNS и провайдерские credentials;
- firmware images.

Сырые backups и firmware хранятся в ignored `personal-it/home-lab/artifacts/openwrt/`, желательно в зашифрованном виде.
