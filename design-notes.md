# Design notes — AgenticSuite redesign (2026-07)

Light-first, premium consumer product site. All visuals are local CSS/SVG
mockups (no stock photos, no remote assets, no vendor logos).

## Tokens

- Paper `#F7F6F3` · surface `#FFFFFF` · ink `#16191F` · muted `#575E69` · hairline `#E8E5DF`
- Brand amber `#F5A623` (fills) / ember `#8F5300` (accessible amber text on light)
- Night palette for console scenes & contrast bands: `#0A0E14` / `#131A26` / `#E6EDF3`
- Status: ok `#1A7F37`, risk `#B3362C` — always paired with a text label, never color alone
- Type: Inter Variable (self-hosted) + IBM Plex Mono for console content only

## Component map

DeviceFrame (browser/phone/console) · PhoneApprovalMock · ACTApprovalCard ·
BrowserBridgeDemo · AgenticKVMDemo · ACTDemo · HermesIntegrationFlow ·
ProductCard · SecurityPill · DemoTimeline · AuditTrail · StatusRail ·
IntegrationChip · SectionHeader · Badge (chip)

Demos are 14–18s CSS keyframe loops. Every animated element uses
`animation-fill-mode: both`, so `prefers-reduced-motion` (which collapses the
animation to a single instant run) rests each scene on its **completed** state.

## Prompts for future generated imagery (drop-in replacements)

- **ACT**: "Premium consumer technology product scene, generic smartphone showing
  a clean approval request for an AI agent action, laptop in background showing
  a completed workflow, soft studio lighting, neutral background, elegant
  minimal composition, no logos, no copyrighted UI." → `public/scene-act.png`
- **BrowserBridge**: "Premium product mockup of an AI agent controlling a generic
  web browser to complete a form, visible cursor path, task checklist, phone
  approval card beside the browser, soft neutral lighting, modern consumer
  technology style, no real brand logos." → `public/scene-browserbridge.png`
- **AgenticKVM**: "Premium product mockup showing a server or VM console recovery
  workflow, generic rack server or compact homelab device, console screen,
  phone approval request, calm high-end technology aesthetic, no vendor
  logos." → `public/scene-agentickvm.png`
- **Hermes integration**: "Elegant abstract integration diagram showing agent
  runtime connected to Hermes, ACT approval layer, BrowserBridge, AgenticKVM,
  and audit log, premium glass cards, soft gradients, clean readable labels,
  no vendor logos." → `public/scene-hermes.png`

## Copy guardrails (carry into any future edit)

- Lead with benefit; keep protocol vocabulary (signed clearances, fail-closed,
  provider registry…) in "How it works → technically curious", Security, and
  Developers sections.
- "Public beta" appears as a small chip and in the footer — never the headline.
- No partnership claims: "integrates with / supports / adapter for / designed
  for / works with compatible environments."
- No guarantees of recovery, safety, or universal hardware/browser support.
- The promise is **controlled agency, not uncontrolled automation** — human
  approval must stay visible in every scene.
