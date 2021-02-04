[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/git/external?repository-url=https%3A%2F%2Fgithub.com%2Fbuilderio%2Fnextjs-shopify)

Next.js + Shopify + Builder.io starter kit.

Demo live at: [headless.builders](https://headless.builders/)

## Goals and Features

- Performant by default
- SEO Ready
- Internationalization
- Responsive
- UI Components
- Theming
- Standardized Data Hooks
- Integrations - Integrate seamlessly with the most common ecommerce platforms.



## Get Started

### Install the Builder.io cli
```
npm install @builder.io/cli -g
```

### Clone this repo
```
git clone https://github.com/BuilderIO/nextjs-shopify.git
```

### Generate your Builder.io space
<!-- TODO: link "private key" to a forum post or doc showing how to create that -->
[Signup for Builder.io](builder.io/signup), then go to your [organization settings page](https://builder.io/account/organization?root=true), create a private key and copy it

```
cd nextjs-shopify
builder create -k [private-key] -n [space-name] -d
```

This command when done it'll print your new space's public api key, copy it and add as the value for `BUILDER_PUBLIC_KEY` into the .env files (`.env.production` and `.env.development`)

```
BUILDER_PUBLIC_KEY=...
```

### Connect Shopify
Now you have a space clone matching the spec defined in this repo, you'll need to connect it to your shopify store.

- Create a [private app](https://help.shopify.com/en/manual/apps/private-apps) in your Shpoify store and generate both admin api keys and storefront API token.

<!-- TODO: how do they get here?? -->
Add these tokens in the `@builder.io/plugin-shopify` settings, if this is your first time it'll pop up asking you for those details.

Add your storefront api token to the .env files (`.env.production` and `.env.development`)

```
SHOPIFY_STOREFRONT_API_TOKEN=dd0057d1e48d2d61ca8ec27b07d3c5e6
SHOPIFY_STORE_DOMAIN=builder-io-demo.myshopify.com
```

### Install dependencies
```
npm i install
```

### Run the dev server
```
npm run dev
```
It'll start a server at `http://localhost:3000`

Go to your [new space settings](https://builder.io/account/space) and change the site url to your localhost `http://localhost:3000` for site editing.


### Deploy

You can deploy anywhere you like, but for this project we recommend [Vercel](https://nextjs.org/docs/deployment). 

For easy deployment just signup for Vercel, connect to this repo, and done!

