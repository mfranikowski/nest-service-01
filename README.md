# NestJS service

Minimal NestJS application ready to be built from a Git repository by Coolify.

## Local development

```sh
npm ci
npm run start:dev
```

The application listens on `http://localhost:3000`. Available endpoints:

- `GET /` returns an example JSON response.
- `GET /health` is used by the container health check.

## Coolify

Create a Docker Compose resource from the repository and select
`compose.coolify.yml` as the compose file. The service is exposed internally on
port `3000`; assign a domain to that port in Coolify.

`Dockerfile.coolify` performs a multi-stage production build and runs the
application as the unprivileged `node` user.
