# Next.js Syllabus — 0 to Advanced

**Prereqs:** JS (ES6+), basic React (components, hooks, props/state), HTML/CSS, Git, terminal basics.
**Format:** Each module has Learn → Build → Checkpoint. Aim 1-2 modules/week, adjust to pace.

---

## Module 0: Setup & Mental Model
- [ ] Install Node LTS, pnpm/npm
- [ ] `npx create-next-app@latest` — explore folder structure (App Router)
- [ ] Understand: Next.js = React framework (routing + rendering + bundling + API layer)
- [ ] File-based routing concept, Server vs Client Components (core Next 13+ shift)
- **Checkpoint:** Explain Server vs Client Components in your own words.

## Module 1: App Router Basics
- [ ] `app/` directory structure: `page.tsx`, `layout.tsx`, `loading.tsx`, `error.tsx`, `not-found.tsx`
- [ ] Nested routing, route groups `(group)`, dynamic segments `[id]`, catch-all `[...slug]`
- [ ] `Link`, `useRouter`, `usePathname`, `useSearchParams`
- [ ] Metadata API (`generateMetadata`, static metadata) for SEO
- **Build:** Multi-page site — home, about, blog list, blog `[slug]` page.
- **Checkpoint:** Add nested layouts + a custom 404 page.

## Module 2: Rendering Strategies
- [ ] Server-Side Rendering (SSR) — default in App Router
- [ ] Static Site Generation (SSG) — `generateStaticParams`
- [ ] Incremental Static Regeneration (ISR) — `revalidate`
- [ ] Client-Side Rendering — when to opt in with `"use client"`
- [ ] Streaming SSR + `Suspense` boundaries
- **Build:** Blog with ISR (revalidate every 60s) + a client-only interactive widget.
- **Checkpoint:** Pick correct rendering strategy for: dashboard, marketing page, product page, live chat. Justify each.

## Module 3: Data Fetching
- [ ] `fetch()` in Server Components (auto caching/dedupe)
- [ ] `cache`, `revalidate`, `no-store` fetch options
- [ ] Parallel vs sequential data fetching, `Promise.all`
- [ ] Third-party DB fetch (direct DB calls from Server Components)
- [ ] Client-side fetching with SWR or React Query (for interactive/live data)
- **Build:** Product listing page pulling from a public API (parallel fetch + streaming).
- **Checkpoint:** Fix a waterfall (sequential → parallel) in given code.

## Module 4: API Routes & Server Actions
- [ ] Route Handlers (`app/api/.../route.ts`) — GET/POST/PUT/DELETE
- [ ] Server Actions — forms without API routes, `"use server"`
- [ ] Form handling: `useFormState`, `useFormStatus`, progressive enhancement
- [ ] Validation (Zod) + error handling patterns
- **Build:** CRUD app (e.g., todo/notes) using Server Actions only, no separate API layer.
- **Checkpoint:** Convert a Server Action into a Route Handler and vice versa.

## Module 5: Styling
- [ ] CSS Modules, global CSS
- [ ] Tailwind CSS setup + config
- [ ] `next/font`, `next/image` optimization
- [ ] Component libraries (shadcn/ui) — pick one, don't rabbit-hole
- **Build:** Restyle Module 1 site with Tailwind + shadcn components, optimized images/fonts.
- **Checkpoint:** Lighthouse score check — image/font optimization impact.

## Module 6: State & Client Interactivity
- [ ] When you actually need client state vs server state
- [ ] Context API for global client state
- [ ] Zustand/Jotai for lighter global state (optional, common in industry)
- [ ] URL as state (search params) pattern
- **Build:** Filterable/sortable product table using URL state.
- **Checkpoint:** Explain why URL state > client state for shareable filters.

## Module 7: Auth
- [ ] Auth strategies: session cookies, JWT
- [ ] NextAuth.js (Auth.js) — providers, callbacks, middleware protection
- [ ] Middleware (`middleware.ts`) — route protection, redirects
- [ ] Role-based access control basics
- **Build:** Add login (Google/GitHub OAuth) + protected `/dashboard` route.
- **Checkpoint:** Explain how middleware intercepts requests before route render.

## Module 8: Database Integration
- [ ] ORM choice: Prisma or Drizzle
- [ ] Connect to Postgres (Supabase/Neon — free tiers)
- [ ] Schema design, migrations
- [ ] Server Components + Server Actions talking directly to DB
- **Build:** Full-stack CRUD app: auth + DB + Server Actions (e.g., expense tracker — ties into your finance interest).
- **Checkpoint:** Write a migration + seed script from scratch.

## Module 9: Performance & Optimization
- [ ] `next/dynamic` — code splitting, lazy loading
- [ ] Bundle analysis (`@next/bundle-analyzer`)
- [ ] Caching layers: Data Cache, Full Route Cache, Router Cache — how they interact
- [ ] `revalidatePath`, `revalidateTag` for on-demand invalidation
- [ ] Core Web Vitals — LCP, CLS, INP fixes
- **Build:** Audit + optimize your Module 8 app (bundle size, cache strategy).
- **Checkpoint:** Diagram Next.js's 4 caching layers from memory.

## Module 10: Testing
- [ ] Unit testing (Vitest/Jest) for utils/components
- [ ] Component testing (React Testing Library)
- [ ] E2E (Playwright) for critical flows (login, checkout)
- **Build:** Add test suite to Module 8 app — cover auth flow + one CRUD path.
- **Checkpoint:** One failing test, debug and fix it.

## Module 11: Deployment & DevOps (ties to your Azure track)
- [ ] Deploy to Vercel (zero-config baseline)
- [ ] Deploy to Azure: App Service or Azure Static Web Apps + Azure Container Apps
- [ ] Environment variables, secrets management
- [ ] CI/CD basics — GitHub Actions for build/test/deploy
- **Build:** Deploy Module 8 app to Azure with a GitHub Actions pipeline.
- **Checkpoint:** Explain differences between Vercel's Next.js runtime and a generic container deployment.

## Module 12: Advanced Topics
- [ ] Parallel routes & intercepting routes (modals, dashboards)
- [ ] Internationalization (i18n) routing
- [ ] Edge runtime vs Node runtime — tradeoffs
- [ ] Monorepo setup (Turborepo) for multi-app projects
- [ ] Advanced SEO: sitemap.xml, robots.ts, structured data (JSON-LD)
- [ ] Web sockets / real-time (optional — Pusher/Ably or raw WS)
- **Checkpoint:** Implement one parallel-route modal pattern (e.g., photo modal over gallery).

## Capstone Project
Build one production-grade app combining everything:
- Auth + role-based access
- DB-backed CRUD with Server Actions
- ISR for public pages, SSR for dashboard
- Tailwind + shadcn UI
- Deployed on Azure with CI/CD
- Test coverage on critical paths

**Suggested capstone (fits your interests):** Personal finance tracker — expense logging, portfolio dashboard, auth, charts, deployed on Azure.

---

## Resources
- Official docs: nextjs.org/docs (App Router section — primary source, changes fast)
- Prisma docs, Auth.js docs, Tailwind docs
- Vercel's Next.js Learn course (free, hands-on)

## Time Estimate
- Fundamentals (0-5): ~4-5 weeks
- Intermediate (6-9): ~4 weeks
- Advanced (10-12) + Capstone: ~3-4 weeks
- **Total: ~11-13 weeks at steady pace**
