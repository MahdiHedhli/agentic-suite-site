# agenticsuite.work

Brand site for the **Agentic Control Suite** — one landing page plus one page per
product (Agentic Control Tower, AgenticKVM, BrowserBridge).

Static, no backend, no secrets, no env vars. Built with [Astro](https://astro.build)
and Tailwind CSS, deployed to Cloudflare Pages on every push to `main`.

## Develop

```sh
npm install
npm run dev      # localhost:4321
npm run build    # static output in dist/
```

## Structure

```
src/
  layouts/Base.astro     # shared shell: head, nav, footer, meta/OG
  components/            # Nav, Footer, SectionHeader, ProductCard, Badge,
                         # DeviceFrame, demo components (BrowserBridge/KVM/ACT),
                         # StatusRail, AuditTrail, IntegrationChip, SecurityPill
  pages/                 # index, act, agentickvm, browserbridge, 404
  styles/tokens.css      # design tokens (palette, type)
  styles/global.css      # base styles + shared component classes
public/                  # favicon, og-image, robots.txt
```

## Deploy

Cloudflare Pages, framework preset **Astro** (`npm run build` → `dist/`).
Custom domain: `agenticsuite.work`.
