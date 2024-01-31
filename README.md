# shadcn/ui + Nx + Next.js

This is a sample project that demonstrates how to use [shadcn/ui](https://ui.shadcn.com/) with [Nx](https://nx.dev/) and [Next.js](https://nextjs.org/).

# Running this project locally

```bash
npx nx serve next-app
```

# Manual setup steps

Commands to generate the project:

```bash
npx create-nx-workspace@latest
npm i -D @nx/next
nx g @nx/next:setup-tailwind --project=next-app
npm i tailwindcss-animate class-variance-authority clsx tailwind-merge
nx g @nx/next:setup-tailwind --project=next-app
npm i lucide-react
```

Copy the following files from this repo to your project:

- [`components.json`](https://github.com/brunos3d/shadcn-ui-nx-next/blob/main/components.json)
- [`tsconfig.json`](https://github.com/brunos3d/shadcn-ui-nx-next/blob/main/tsconfig.json)
- [`tsconfig.base.json`](https://github.com/brunos3d/shadcn-ui-nx-next/blob/main/tsconfig.base.json)
- [`apps/next-app/tailwind.config.js`](https://github.com/brunos3d/shadcn-ui-nx-next/blob/main/apps/next-app/tailwind.config.js)

# Installing new shadcn/ui components

After following the installation steps above, installing [shadcn/ui components](https://ui.shadcn.com/docs/components) is a simple task and requires the following steps

```bash
npx shadcn-ui@latest add <component> # e.g button
```

Add/Export the new component to `libs/shadcn-ui/src/index.ts`

```bash
export * from './components/ui/command';
```

Now, you're able to use your component on your Nx Project

```bash
import { Button } from '@libs/shadcn-ui';
```
