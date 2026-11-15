# nexy-jobs

Background jobs, queues and scheduled tasks for Nexy apps, with nothing extra to install to start.

## Why

Sending an email after sign-up, resizing an upload, a nightly cleanup: each needs work outside the
request. Today that means adding Celery or RQ, a Redis server and a second process. nexy-jobs starts
with the database the project already has and grows to Redis when the load asks for it.

## What it covers

| Area | First version |
|---|---|
| Jobs | a decorated function, enqueued from a handler or an action, with typed arguments |
| Reliability | retries with backoff, timeouts, dead letters, idempotency keys |
| Schedules | cron expressions and intervals declared next to the function |
| Backends | the project database (PostgreSQL, SQLite), then Redis |
| Workers | started by `nexy dev` and `nexy start`, or alone with `nx jobs` |
| Visibility | a dev page listing queued, running and failed jobs |

## Status

Design phase. Nothing is published yet.

## License

MIT
