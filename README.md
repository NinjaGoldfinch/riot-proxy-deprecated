# depreciated

> [!WARNING]
> **This repository is deprecated and no longer maintained.** It was previously
> `riot-proxy`. Development has moved to a new repository. Nothing here
> receives fixes, dependency updates or security patches, and issues and pull
> requests will not be looked at.

---

## What this was

`riot-proxy` was a self-hosted middleman API between Riot Games' public API and
downstream projects (websites, Discord bots, CLIs, analytics). It held the Riot
key in one place, cached aggressively, centralised Riot's rate limiting, and
gave consumers a stable internal contract. It was built on Fastify, Redis,
Postgres and BullMQ.

## Where things are

| What                   | Where                                                    |
| ---------------------- | -------------------------------------------------------- |
| Full original README   | [`docs/ARCHIVED-README.md`](docs/ARCHIVED-README.md)     |
| Spec it implemented    | [`docs/riot-proxy-spec.md`](docs/riot-proxy-spec.md)     |
| Roadmap at deprecation | [`TODO.md`](TODO.md)                                     |
| OpenAPI document       | [`openapi.json`](openapi.json)                           |
| Code                   | [`src/`](src/) — left as it was, but will not be updated |

## If you still run it

- **Stop and migrate.** Dependencies will age out and nothing will patch them.
- **Revoke the Riot API key** held by any running deployment once it is shut
  down, and delete any consumer keys (`rpx_…`) you minted for it.
- The scheduled nightly acceptance run has been removed so the archive does not
  spend Riot quota or fail on an expired key.

## Compliance

`riot-proxy` isn't endorsed by Riot Games and doesn't reflect the views or
opinions of Riot Games or anyone officially involved in producing or managing
Riot Games properties.

## Licence

Private. Not for redistribution.
