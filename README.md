# cosmocloud-deploy

This Helm Chart deploys a backend, frontend, and Redis database as a single application stack.

## Components

- **Backend**: Deployed using the image `shrey batra/sample-backend` with the environment variable `REDIS_URI` set to `redis://redis-svc:6379`.
- **Frontend**: Deployed using the image `shreybatra/sample-frontend` with the environment variable `BACKEND_URL` set to `http://backend-svc:8000`.
- **Redis**: Deployed using the official Redis image.

## Installation

To install the Helm Chart, run the following command:

```bash
helm install testapp cosmocloud-deploy --atomic --timeout 30s
