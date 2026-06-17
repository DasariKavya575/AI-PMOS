# AI-PMOS: Enterprise AI Program Management Operating System

AI-PMOS is a production-grade reference platform for an AI-powered Executive Copilot that gives global leaders real-time visibility into programs, delivery risk, financial impact, resource utilization, and strategic blockers.

## What Is Included

- FastAPI backend with Pydantic v2, SQLAlchemy async boundaries, JWT auth, RBAC, Prometheus metrics, and OpenTelemetry hooks.
- React TypeScript executive dashboard with portfolio health, risk, finance, resources, forecasts, and AI operations signals.
- Enterprise integration boundaries for Jira, Slack, Salesforce, Confluence, GitHub, and ServiceNow-style incremental sync.
- RAG architecture for PDF, DOCX, PPTX, Jira, Slack, hybrid retrieval, metadata filtering, reranking, and context compression.
- LangGraph multi-agent orchestration scaffold for program, risk, finance, resource, prediction, executive reporting, and governance agents.
- Forecasting service boundary for XGBoost, LightGBM, and Prophet-backed models.
- Docker Compose, Kubernetes manifests, Terraform EKS module, GitHub Actions, Grafana dashboard, API and event contracts.

## Repository Structure

```text
apps/
  api/                 Python 3.12 FastAPI service
  web/                 React TypeScript executive dashboard
contracts/
  api/                 OpenAPI contract summaries
  events/              Kafka JSON Schema contracts
docs/
  architecture.md      Architecture, database, API, security, and phase plan
  deployment.md        Local, Kubernetes, and AWS EKS deployment guide
  evaluation.md        RAG, agent, and forecasting evaluation framework
infra/
  docker/              API and web Dockerfiles
  k8s/                 Kubernetes manifests
  terraform/           AWS EKS Terraform module and prod environment
observability/
  grafana/dashboards/  Grafana dashboards
```

## Local Development

```bash
docker compose up --build
```

API: `http://localhost:8000`  
Swagger: `http://localhost:8000/docs`  
Web: `http://localhost:8080`

## Backend Tests

```bash
cd apps/api
pip install -e ".[dev]"
pytest
```

## Core Executive Questions

- Show top risks affecting quarterly revenue.
- Which projects are likely to miss deadlines?
- Which teams are overloaded?
- Predict budget overruns.
- Generate executive summaries.
- Identify blockers affecting strategic objectives.

## Production Notes

This is a production scaffold, not a toy app. The code establishes deployable boundaries, contracts, security posture, observability hooks, and extension points. Real enterprise rollout would add source-system credentials, private networking, managed RDS/MSK/ElastiCache, model registry promotion gates, fine-grained tenant isolation, and SOC2-aligned operational controls.
