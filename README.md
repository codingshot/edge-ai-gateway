# Edge AI Gateway
This is the Edge Intelligence Summit Gateway

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fcodingshot%2Flinktree-bos&build-command=pnpm%20run%20build&env=NEXT_PUBLIC_NETWORK_ID,NEXT_PUBLIC_HOSTNAME,NEXT_PUBLIC_ACCOUNT_ID,NEXT_PUBLIC_THEME&envDescription=mainnet-near.org-themecanbeanything&envLink=https%3A%2F%2Fgithub.com%2Fcodingshot%2Flinktree-bos%2Fblob%2Fmain%2F.env.example) 


To setup a custom domain on vercel

https://vercel.com/docs/concepts/projects/domains/add-a-domain

## Setup & Development

Initialize repo:

```bash
pnpm i
```

Start development version:

```bash
cp .env.example .env
pnpm dev
```

The entry component is ```Edge.Views.Home``` and it's located at
```/src/components/polygon/index.tsx```

It loads the ```edgeai.near/widget/Edge.Views.Home``` BOS component. The source can be found [here](https://near.org/near/widget/ComponentDetailsPage?src=edgeai.near/widget/Edge.Views.Home&tab=source).

## Deployment

This is a [Next.js](https://github.com/vercel/next.js/) app and a fork of [NEAR Discovery](https://github.com/near/near-discovery) gateway app.

For static exports just run ```next build``` and upload the build files to your hosting provider. More info [here](https://nextjs.org/docs/pages/building-your-application/deploying/static-exports).

For Vercel, Cloudflare or others that supports a Next app just connect the repo and follow the deploy steps from the dashboards.

More info on Next.js deployments [here](https://nextjs.org/docs/pages/building-your-application/deploying/static-exports).

## Running with docker

```bash
docker build -t linktree-bos .
docker run -p 3000:3000 linktree-bos
```
