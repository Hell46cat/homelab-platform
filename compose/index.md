# Compose

Production Docker Compose definitions for services running on the mini-PC.

Add a service only after documenting its purpose, persistent data, health check, update procedure, rollback and restore test. Host-specific secrets are loaded from `/etc/homelab` and are never committed.
