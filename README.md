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

- `components.json`
- `tsconfig.json`
- `tsconfig.base.json`
- `apps/next-app/tailwind.config.js`
