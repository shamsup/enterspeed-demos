# SvelteKit demo

Everything you need to build a Svelte project, powered by [`create-svelte`](https://github.com/sveltejs/kit/tree/master/packages/create-svelte).

## Cloning this demo

To clone a single folder use Git Bash.

```bash
git clone \
  --depth 1  \
  --filter=blob:none  \
  --sparse \
  https://github.com/enterspeedhq/enterspeed-demos \
;
cd enterspeed-demos
git sparse-checkout set sveltekit
```

## Developing

Once you've cloned this and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Environment Variables

To run this project, you will need to add the following environment variables to your .env file

`VITE_ENTERSPEED_PRODUCTION_ENVIRONMENT_API_KEY`

## What you'll need

You will need to set up a free Enterspeed account. You can sign up here: https://app.enterspeed.com/signup

Once you have created your account and created a tenant, you need to configure your tenant by setting up:
Domains and hostnames
Environment and environment clients
Data sources
You can read more about it in our getting started guide: https://docs.enterspeed.com/getting-started

### Ingesting dummy data

Once you have created a data source in Enterspeed, you can start ingesting data. This can be done using our API: https://docs.enterspeed.com/api#tag/Ingest

You can find the data used in the demos here: [enterspeed-dummy-data](https://github.com/enterspeedhq/enterspeed-demos/tree/master/enterspeed-dummy-data)

#### Example ingest

```curl
curl --location --request POST 'https://api.enterspeed.com/ingest/v2/UNIQUE-ID' \
--header 'X-Api-Key: [INSERT-YOUR-OWN-API-KEY]' \
--header 'Content-Type: application/json' \
--data-raw '{
  "type": "blog",
  "url": "/blog"
}'
```
