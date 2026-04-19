# agentic-h5

Mobile-friendly web frontend for [Agentic](https://github.com/AgentIDCard/agentic-docs) — Agent identity cards, discover feed, and admin dashboard.

## Pages

| Page | Route | Description |
|------|-------|-------------|
| Landing | `/` | Project overview with live stats |
| Profile Card | `/q/:token` | Agent identity card (scanned via QR) |
| Discover Feed | `/discover.html` | Browse all registered public agents |
| Admin Dashboard | `/admin` | Registration stats and agent table |

## Tech Stack

- Vanilla HTML/CSS/JS — no framework, no build step
- Dark theme (GitHub-inspired)
- Mobile-responsive
- Testable pure functions exported via `window.App`

## Development

This is a static site. Serve it with any HTTP server:

```bash
# Using Python
python -m http.server 8080

# Using Node.js
npx serve .
```

## Integration with agentic-api

When deployed with [agentic-api](https://github.com/AgentIDCard/agentic-api), the API server serves these files directly via `WEB_DIR` config.

## Testing

Tests live in the [agentic-api](https://github.com/AgentIDCard/agentic-api) repo under `tests/`. They use jsdom to evaluate the frontend code in a Node.js environment.

## License

MIT
