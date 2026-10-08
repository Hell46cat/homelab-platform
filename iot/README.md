# IoT & Smart Home Configurations

Конфигурации, исходники прошивок и бэкапы настроек умных контроллеров и микроконтроллеров хоумлаба.

## Структура

```text
iot/
├── esphome/               # YAML-конфигурации прошивок ESPHome (ESP32 / ESP8266)
│   ├── devices/           # Конфиги конкретных устройств (*.yaml)
│   └── secrets.example.yaml # Шаблон Wi-Fi и API ключей (secrets.yaml игнорируется)
└── wled/                  # Бэкапы пресетов и конфигов контроллеров WLED
    └── homeled/           # Экспорты presets.json и cfg.json для подсветки
```

Документация по железу, распиновке и IP-адресам: [13-iot-inventory.md](../../homelab-wiki/home-lab/docs/13-iot-inventory.md).
