# NOVA Commerce

A premium South African ecommerce foundation rebuilt from the original `website-ios` project.

## Included
- Next.js 16 App Router
- TypeScript
- Tailwind-free custom responsive UI
- PostgreSQL + Prisma schema
- Product/variant/inventory models
- Persistent client cart
- Server-side checkout validation
- Transactional inventory decrement
- ZAR pricing and South African province fields
- VAT calculation
- Customer/admin roles and signed sessions foundation
- CI workflow
- SEO metadata foundation

## Local setup
1. Install Node.js 20+ and PostgreSQL.
2. Copy `.env.example` to `.env`.
3. Set `DATABASE_URL` and a strong `AUTH_SECRET`.
4. `npm install`
5. `npx prisma db push`
6. `npm run db:seed`
7. `npm run dev`

Seed admin: `admin@example.com` / `ChangeMeImmediately123!` — change this before production.

## Production blockers
The payment provider is intentionally MOCK. Connect a real provider and verify signed webhooks before accepting money. Also configure email, shipping/carrier rates, monitoring, backups, privacy/returns/tax compliance and real product imagery.
