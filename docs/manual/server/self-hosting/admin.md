---
hide:
  - toc
---

# Administration

asciinema server provides admin panel on port 4002, separate from the main,
user-facing web interface.

To be able to access the admin panel when deploying the container make sure
this port is exposed.

```yaml title="docker-compose.yml"
services:
  asciinema:
    ports:
      - '4002:4002'
```

!!! danger

    At the moment the admin endpoint doesn't perform any form of
    authentication/authorization so do not expose this port directly to the
    internet when running a public asciinema server instance.
