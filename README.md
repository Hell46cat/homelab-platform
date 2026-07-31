# homelab-platform

Deployment repository for the mini-PC. It owns production Docker Compose definitions, Ansible automation, operational scripts and recovery instructions.

Architecture decisions and learning notes remain in the parent `personal-it` repository under `home-lab/docs/`. Application source code lives in separate repositories under `apps/` on the main PC.

## Repository layout

```text
homelab-platform/
├── compose/       production service definitions
├── ansible/       repeatable host configuration
├── scripts/       small explicit operational helpers
├── docs/          platform runbooks and technical reference
├── .env.example   documented non-secret variable names
└── README.md
```

## Server paths

```text
/opt/homelab-platform/     this Git checkout
/srv/home-lab/<service>/    persistent data
/etc/home-lab/<service>.env secrets and machine-specific settings
```

Secrets, real `.env` files, private keys, database files and backups are never committed.

## Initial deployment

The repository is intentionally scaffolded before the mini-PC arrives. Service definitions are added one at a time after a manual local test and a documented rollback path.

See the parent vault page `home-lab/docs/development-and-deployment.md` for the full development and delivery workflow.


