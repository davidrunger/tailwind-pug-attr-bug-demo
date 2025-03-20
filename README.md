# tailwind-pug-attr-bug-demo

This repo demonstrates a bug in `tailwindcss` v4.0.15 where not all expected Tailwind classes are extracted from a Pug template in a Vue component.

## Project Setup

(I tested this with `pnpm` version 10.6.5.)

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

Check out the second-most-recent commit in this repo, which has `tailwindcss` and `@tailwindcss/vite` at 4.0.9:

```sh
git checkout main^
```

Install the older Tailwind packages (at 4.0.9):

```sh
pnpm install --frozen-lockfile
```

Run the `pnpm dev --force` and/or `pnpm build && pnpm preview` commands mentioned above. When viewing the relevant URLs (http://localhost:5173/ and http://localhost:4173/, respectively), you should now see a black background behind the "This div has an HTML attribute." text.
