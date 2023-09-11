# Deno Nuxt Template

This template application uses
[Nuxt 3](https://nuxt.com/docs/getting-started/introduction) and provides a
starting point for using Nuxt on [Deno Deploy](https://deno.com/deploy).

## Local development

Begin by installing the dependencies for the project:

```bash
npm install
```

Start the development server on `http://localhost:3000`:

```bash
npm run dev
```

## Run on Deno Deploy

This repo contains a GitHub workflow configuration to automatically deploy your
application when you push to the main branch.

Before deploying for the first time, edit `.github/workflows/deploy.yml` and
include your project ID near the bottom of this file.

### Previewing production build

To preview the production version of the application, build the site with this
command:

```bash
NITRO_PRESET=deno_deploy npm run build
```

Then, run the server:

```bash
cd .output
deno run -A --unstable server/index.ts
```

Check out the
[Nuxt 3 deployment docs](https://nuxt.com/docs/getting-started/deployment) for
more information.

## License

MIT
