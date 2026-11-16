# VSPARK Portal

Competition-day portal for the VSPARK Prompt Engineering Competition (AI Video Generation Challenge) at COMSATS University Islamabad, Vehari Campus.

## Run locally

```bash
npm install
copy .env.example .env
npm start
```

- Landing page: http://localhost:3000
- Registration: http://localhost:3000/register
- Participant portal: http://localhost:3000/portal
- Admin: http://localhost:3000/admin (default `admin` / `admin123` unless `ADMIN_USER` and `ADMIN_PASSWORD` are set)

If `MONGODB_URI` is unset, data is stored in `data/`. Receipt files go in `data/receipts/`.

In production (`NODE_ENV=production`) the server refuses to start unless `ADMIN_PASSWORD` is set.

## Pages

- `/` landing page, including winners after results are published
- `/register` team registration with a payment receipt (JPG, PNG, or PDF, max 2 MB)
- `/portal` participant login with Registration ID plus a member registration number
- `/admin` registrations, settings, live timer, and results

Each accepted team gets a configurable window (`COMPETITION_MINUTES`, default 20) once an admin opens the gate.
