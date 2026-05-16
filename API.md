# API Reference

StarsCashFlow exposes a public partner API for integrations.

- **Base URL:** `https://api-stars.ros.media`
- **Recommended endpoint:** `POST /api/v2`
- **Backward-compatible endpoint:** `POST /api`

Interactive documentation is available at `/docs` on the API host, and a public FAQ at `/faq`.

## Authentication

Requests are authenticated with an API key issued to a partner account. The key is passed as a request parameter.

## Actions

The API uses an `action` parameter to select the operation:

| Action | Description |
|---|---|
| `services` | List available services |
| `balance` | Get current account balance |
| `add` | Create a new order |
| `status` | Check the status of an order |
| `cancel` | Cancel an order |

### Example request

```
POST /api/v2
key=API_KEY&action=add&service=1&link=https://t.me/your_channel&quantity=100
```

## Public endpoints

| Path | Description |
|---|---|
| `/` | API landing page |
| `/docs` | Interactive API documentation |
| `/faq` | Public FAQ |
| `/market` | Public services catalog |
| `/healthz` | Health check |
| `/robots.txt`, `/sitemap.xml` | SEO files |

## Notes

- Use `POST /api/v2` for new integrations; `POST /api` is kept for backward compatibility.
- Order parameters typically include `service`, `link` and `quantity`.
