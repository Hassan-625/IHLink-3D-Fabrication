# IHLink 3D Fabrication Lab

Standalone prototyping, CAD-support and fabrication-service platform.

## Platform role

- **Platform key:** `fabrication`
- **Frontend:** standalone repository
- **Backend:** shared IHLink Supabase project
- **Administration:** IHLink Command Center
- **Deployment:** Vercel

## Core capabilities

- 3D printing and prototyping requests
- CAD and product-design support
- Material, process, dimensions and quantity specifications
- Custom parts and project enclosures
- Fabrication job and production tracking
- Quotations, invoices, payments, files and support

## Architecture

Fabrication customer requests and production jobs are tracked separately. The customer defines the required specification while authorized operations staff manage fabrication status and delivery records.

The platform uses shared IHLink authentication and backend services while retaining its own customer-facing routes, platform authorization and specialist workflow.

## Technology

- React
- TypeScript
- Vite
- Tailwind CSS
- React Router
- Supabase
- Vercel

## Local development

```bash
npm install
npm run dev
```

Build for production with `npm run build`. Where configured, run `npm run typecheck` and `npm run lint` before release.

## Environment and secrets

Configure public client values such as `VITE_SUPABASE_URL` and `VITE_SUPABASE_ANON_KEY` through environment configuration. Cross-platform origin variables may be configured where IHLink handoff is required.

Never commit service-role credentials, payment/provider secrets, private API keys or webhook secrets.

## Data and security

Customer records are protected through Supabase Row Level Security and server-side workflows. Privileged operational changes and payment settlement must remain server-authorized. Specialist data must not become writable merely because an account is generally active.

## IHLink ecosystem integration

The application is a standalone IHLink platform connected to the shared backend and central Command Center. Authentication may be shared, but platform/service authorization remains explicit.

## Deployment

Production is deployed through the IHLink Vercel team. Verify production routing, environment configuration and core authenticated flows after each release.

## Ownership

**IHLink Co. Ltd.**  
Copyright © 2026 IHLink Co. Ltd. All rights reserved.
