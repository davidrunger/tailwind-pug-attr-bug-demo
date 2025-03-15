# tailwind-pug-bug-demo

This repo demonstrates a bug in `tailwindcss` v4.0.14 (and some earlier versions) where not all expected Tailwind classes are extracted from a Pug template in a Vue component.

## Project Setup

(Tested with `pnpm` version 10.6.3.)

```sh
pnpm install --frozen-lockfile
```

### Compile and Hot-Reload for Development

```sh
pnpm dev --force
```

### Compile for production and launch server

```sh
pnpm build && pnpm preview
```

## Go back to a Tailwind version that doesn't have this bug

Check out the first commit in this repo, which has `tailwindcss` and `@tailwindcss/vite` at 4.0.9:

```sh
git checkout `git rev-list --max-parents=0 HEAD | tail -n 1`
```

Install those older packages:

```sh
pnpm install --frozen-lockfile
```

Run the `pnpm dev --force` and/or `pnpm build && pnpm preview` commands mentioned above. When viewing the relevant URLs (http://localhost:5173/ and http://localhost:4173/, respectively), you should now see a black background behind the "This is a test." text.
