# Private AI in a Box — Third-Party Notices

Private AI in a Box (SKU PAIB-01) is built from open-source components. This
document lists every third-party component the product deploys, the version
delivered, its licence, and where to read that licence.

The deployment template installs these components into your own Azure
subscription, pulled directly from their upstream registries at deployment
time. Data Meaning Services Group, Inc. does not distribute, mirror, or
republish them. Each component is deployed unmodified, and all copyright and
licence notices are retained.

The OCR service adapter is authored by Data Meaning Services Group, Inc. and
is supplied from a registry we operate, `datameaning.azurecr.io`. Its
container image is built on a third-party base image, which is identified
below along with the source for its components. Every other third-party
component is pulled from its publisher's own registry.

---

## Container images

Components are pinned either by content digest or by exact version, so the
software delivered is the software listed here.

Where a component publishes no version number, the entry gives the build
identifier, which is the source commit the image was built from. That
identifies the code more precisely than a release number.

| Component | Version | Licence | Licence text |
|---|---|---|---|
| vLLM | 0.26.0 | Apache-2.0 | https://github.com/vllm-project/vllm/blob/main/LICENSE |
| LibreChat | 0.8.6 | MIT | https://github.com/danny-avila/LibreChat/blob/main/LICENSE |
| MongoDB | 7.0.39 | SSPL-1.0 | https://www.mongodb.com/licensing/server-side-public-license |
| Redis | 7.4.10 | RSALv2 / SSPLv1 | https://redis.io/legal/licenses/ |
| RabbitMQ | 3.13.7 | MPL-2.0 | https://github.com/rabbitmq/rabbitmq-server/blob/main/LICENSE-MPL-RabbitMQ |
| PostgreSQL | 16.14 | PostgreSQL Licence | https://www.postgresql.org/about/licence/ |
| pgvector | 0.8.6 | PostgreSQL Licence | https://github.com/pgvector/pgvector/blob/master/LICENSE |
| Text Embeddings Inference | 1.8.3 | Apache-2.0 | https://github.com/huggingface/text-embeddings-inference/blob/v1.8.3/LICENSE |
| LibreChat RAG API | build `d6db3e38` | MIT | https://github.com/danny-avila/rag_api/blob/main/LICENSE |
| speaches (speech to text) | 0.8.3 | MIT | https://github.com/speaches-ai/speaches/blob/master/LICENSE |
| faster-whisper | 1.1.1 | MIT | https://github.com/SYSTRAN/faster-whisper/blob/master/LICENSE |
| SearXNG | 2026.8.4 | AGPL-3.0-or-later | https://github.com/searxng/searxng/blob/master/LICENSE |
| Firecrawl | build `6ff68d3b` | AGPL-3.0 | https://github.com/firecrawl/firecrawl/blob/main/LICENSE |
| Firecrawl Playwright service | build `468009ba` | AGPL-3.0 | https://github.com/firecrawl/firecrawl/blob/main/LICENSE |
| Firecrawl Postgres service | build `aed86f62` | AGPL-3.0 | https://github.com/firecrawl/firecrawl/blob/main/LICENSE |
| PostgreSQL (Firecrawl service) | 17.10 | PostgreSQL Licence | https://www.postgresql.org/about/licence/ |
| Playwright | 1.58 | Apache-2.0 | https://github.com/microsoft/playwright/blob/main/LICENSE |
| Tesseract OCR | 5.5.1 | Apache-2.0 | https://github.com/tesseract-ocr/tesseract/blob/main/LICENSE |
| tesseract-server | build `29f62caf` | MIT | https://github.com/hertzg/tesseract-server/blob/master/LICENSE |
| Prometheus | 2.54.1 | Apache-2.0 | https://github.com/prometheus/prometheus/blob/main/LICENSE |
| Grafana | 11.2.0 | AGPL-3.0 | https://github.com/grafana/grafana/blob/main/LICENSE |
| NVIDIA Kubernetes device plugin | 0.15.0 | Apache-2.0 | https://github.com/NVIDIA/k8s-device-plugin/blob/main/LICENSE |

## Cluster components

Installed from the publishers' released manifests at the versions shown.

| Component | Version | Licence | Licence text |
|---|---|---|---|
| ingress-nginx | 1.11.2 | Apache-2.0 | https://github.com/kubernetes/ingress-nginx/blob/main/LICENSE |
| cert-manager | 1.15.3 | Apache-2.0 | https://github.com/cert-manager/cert-manager/blob/master/LICENSE |

## Models

Model weights are downloaded from Hugging Face at deployment time and are
separate works from the software that serves them.

| Model | Purpose | Licence | Licence text |
|---|---|---|---|
| `openai/gpt-oss-120b` | Language model | Apache-2.0 | https://huggingface.co/openai/gpt-oss-120b |
| `BAAI/bge-small-en-v1.5` | Text embeddings | MIT | https://huggingface.co/BAAI/bge-small-en-v1.5 |
| `Systran/faster-whisper-base.en` | Speech to text | MIT | https://huggingface.co/Systran/faster-whisper-base.en |

## Components authored by Data Meaning Services Group, Inc.

| Component | Description |
|---|---|
| OCR service adapter | Translates document OCR requests to the in-cluster Tesseract service. |
| Deployment template and configuration | Azure Resource Manager template, deployment configuration, and Kubernetes manifests. |

These are supplied by Data Meaning Services Group, Inc. under the terms of
your agreement.

### Third-party libraries used by the OCR service adapter

| Library | Version | Licence | Licence text |
|---|---|---|---|
| FastAPI | 0.115.6 | MIT | https://github.com/fastapi/fastapi/blob/master/LICENSE |
| Uvicorn | 0.34.0 | BSD-3-Clause | https://github.com/encode/uvicorn/blob/master/LICENSE.md |
| HTTPX | 0.28.1 | BSD-3-Clause | https://github.com/encode/httpx/blob/master/LICENSE.md |
| Python | 3.12 | PSF-2.0 | https://docs.python.org/3/license.html |

The OCR service adapter's container image is built on the official
`python:3.12-slim` base image, which is Debian GNU/Linux. That base contains
Debian system packages under a range of licences, including GPL-2.0 and
GPL-3.0 for parts of the base system. Complete corresponding source for every
Debian package is published by the Debian Project at
https://sources.debian.org/, and Data Meaning Services Group, Inc. will
provide the corresponding source for any package in this image on request to
legal@datameaning.com.

---

## Copyleft components

The following components are licensed under copyleft terms. Each is deployed
unmodified from its publisher's own registry, and its complete corresponding
source is published by the copyright holder at the repository shown.

| Component | Licence | Source |
|---|---|---|
| SearXNG | AGPL-3.0-or-later | https://github.com/searxng/searxng |
| Firecrawl, and its Playwright and Postgres services | AGPL-3.0 | https://github.com/firecrawl/firecrawl |
| Grafana | AGPL-3.0 | https://github.com/grafana/grafana |
| RabbitMQ | MPL-2.0 | https://github.com/rabbitmq/rabbitmq-server |
| MongoDB | SSPL-1.0 | https://github.com/mongodb/mongo |
| Redis | RSALv2 / SSPLv1 | https://github.com/redis/redis |

---

Component versions were read from the deployed containers. Image digests for
each component are available on request.

For questions about this document, contact legal@datameaning.com.

*Last updated: 8 August 2026*
