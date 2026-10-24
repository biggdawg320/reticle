### Fixed

- **`@reticlehq/server` — in a project with no Reticle wiring, agents started a second dev server.** The first instructions told the agent to lease `"<the running app's URL>"` and did not say where to find that URL. Agents started their own dev server on a new port, leased it, and sometimes left it running. The instructions now say to take the URL from `next_step.lease` in `reticle_session { action: "list" }`, which names the user's running dev server, and not to start a second one.
