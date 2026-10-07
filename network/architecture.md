# Network configuration boundary

Каноническая архитектура домашней сети, этапы миграции, VLAN-план и firewall-решения находятся в [[home-lab/docs/12-network-architecture|personal-it/home-lab/docs/12-network-architecture.md]].

Этот репозиторий хранит только применяемую техническую реализацию:

- sanitized-конфиги без секретов;
- scripts проверки и применения;
- operational runbooks;
- rollback-процедуры.

Архитектурные решения здесь не дублируются. Если реализация расходится с канонической заметкой, сначала фиксируется новое решение в `personal-it`, затем обновляется конфигурация `homelab-platform`.
