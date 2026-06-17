# GuideSite

GuideSite is a Sanity-powered Next.js site in a Turborepo monorepo.

## What is included

### Apps

- `apps/web`: Next.js frontend
- `apps/studio`: Sanity Studio

### Packages

- `packages/ui`: shared UI components
- `packages/sanity`: shared Sanity clients, GROQ queries, live preview utilities, and image helpers
- `packages/env`: environment variable helpers
- `packages/logger`: shared logger utility
- `packages/typescript-config`: shared TypeScript configuration

## Features

- Next.js App Router with TypeScript
- Sanity Studio v5
- Visual editing and live preview support
- Shadcn UI components with Tailwind CSS
- Blog, FAQ, page, navigation, footer, and settings schemas
- Type-safe GROQ queries with generated TypeScript types
- Turborepo build orchestration and caching

## Getting started

### 1. Install dependencies

```shell
pnpm install
```

### 2. Run the web app and Studio locally

```shell
pnpm run dev
```

Open the web app at [http://localhost:3000](http://localhost:3000).

Open the Studio at [http://localhost:3333](http://localhost:3333).

## Working with content

### Create content

The Sanity schema includes `Author`, `Blog`, `BlogIndex`, `FAQ`, `Footer`, `HomePage`, `Navbar`, `Page`, and `Settings` document types.

From the Studio, click "+ Create", choose a document type, then create and publish content. Published content appears in the web app and in the Studio Presentation tool.

### Seed local content

To import the bundled seed data into the production dataset:

```shell
cd apps/studio
npx sanity dataset import ./seed-data.tar.gz production --replace
```

### Extend the schema

Document schemas live in `apps/studio/schemaTypes/documents`.

Shared frontend Sanity utilities live in `packages/sanity`.

## Deployment

### Deploy Sanity Studio

Run the first Studio deploy locally from `apps/studio`:

```shell
npx sanity deploy
```

Sanity creates the deployed Studio application and returns an app ID. Set that value as `SANITY_STUDIO_APP_ID` locally and in GitHub repository secrets so later CI deploys target the same Studio.

The GitHub Actions workflow in `github/workflows/deploy-sanity.yml` deploys the Studio when changes are pushed to the Studio app.

Configure these repository secrets before using CI deploys:

- `SANITY_DEPLOY_TOKEN`
- `SANITY_STUDIO_PROJECT_ID`
- `SANITY_STUDIO_DATASET`
- `SANITY_STUDIO_TITLE`
- `SANITY_STUDIO_PRESENTATION_URL`
- `SANITY_STUDIO_APP_ID`

Set `SANITY_STUDIO_PRESENTATION_URL` to the deployed web app URL. Local development uses `http://localhost:3000`.

To use live preview, the browser must allow third-party cookies.

### Deploy the web app

Deploy `apps/web` to your hosting provider. For Vercel:

1. Create a new Vercel project connected to the repository.
2. Set the root directory to `apps/web`.
3. Configure the required environment variables.

### Configure CORS origins

Production web URLs must be added to the Sanity project's CORS origins.

1. Go to [Sanity Manage](https://www.sanity.io/manage), select the project, then open **API** > **CORS origins**.
2. Add the production URL.
3. Add any custom domains.
4. Keep `http://localhost:3000` for local development.
5. Enable **Allow credentials** for origins that need authenticated requests, such as live preview or visual editing.

For Vercel preview deployments, add specific preview URLs or a wildcard origin for the preview domain pattern.

### Invite collaborators

Open [Sanity Manage](https://www.sanity.io/manage), select the project, then invite project members.
