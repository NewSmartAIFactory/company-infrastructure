# company-infrastructure

Infrastructure for NewSmartAIFactory.

Local compose services:

- PostgreSQL
- Redis
- Qdrant
- RabbitMQ

Start the infrastructure dependencies from this directory:

```powershell
docker compose up -d postgres redis qdrant rabbitmq
```

Verify Qdrant is ready:

```powershell
Invoke-RestMethod http://localhost:6333/collections
```

The API and dashboard run from their own repositories. Prometheus and Grafana
remain planned extensions of the local stack.
