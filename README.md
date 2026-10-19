# Raag

Your AI-powered personal health OS - labs, wearables, records, medications,
and family history unified into one calm, AI-guided view. Raag remembers
your health over time and helps you understand the bigger picture, rather
than treating every visit as a blank slate.


## Stack

TanStack Start (React 19) + TanStack Router/Query + Vite + Tailwind v4 +
Radix UI on the frontend. Supabase (Postgres + Auth + Storage + Edge
Functions) on the backend. Anthropic Claude for document parsing and the
AI assistant. Razorpay for billing.

Everything in the UI reads/writes through `@/lib/queries` →
`src/lib/api/contract.ts` (the `RaagApi` interface) → one of three
adapters selected by `VITE_API_MODE`: `mock` (in-memory demo, no backend
needed), `supabase` (real, persisted - what's actually deployed), `http`
(unused stub for a hypothetical non-Supabase backend).

### Deployment


