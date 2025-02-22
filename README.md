# Prostore

[![Vercel Production](https://github.com/nodejs-devops/prostore-ecommerce/actions/workflows/production.yml/badge.svg)](https://github.com/nodejs-devops/prostore-ecommerce/actions/workflows/production.yml)

A full featured Ecommerce website built with Next.js, TypeScript, PostgreSQL and Prisma.

<img src="/public/images/screen.png" alt="Next.js Ecommerce" />

This project is from my **Next.js Ecommerce course**

- Traversy Media: https://www.traversymedia.com/nextjs-ecommerce
- Udemy: https://www.udemy.com/course/nextjs-ecommerce-course

## Features

- Next Auth authentication
- Admin area with stats & chart using Recharts
- Order, product and user management
- User area with profile and orders
- Stripe API integration
- PayPal integration
- Cash on delivery option
- Interactive checkout process
- Featured products with banners
- Multiple images using Uploadthing
- Ratings & reviews system
- Search form (customer & admin)
- Sorting, filtering & pagination
- Dark/Light mode
- Much more

## Create New Project

1. Create new Next.js Project

   ```sh
   npx create-next-app@latest
   ```

   √ What is your project named? » e-commerce<br>
   √ Would you like to use TypeScript? » No / <u>Yes</u><br>
   √ Would you like to use ESLint? » No / <u>Yes</u><br>
   √ Would you like to use Tailwind CSS? ... No / <u>Yes</u><br>
   √ Would you like your code inside a `src/` directory? » <u>No</u> / Yes<br>
   √ Would you like to use App Router? (recommended) » No / <u>Yes</u><br>
   √ Would you like to use Turbopack for `next dev`? » <u>No</u> / Yes<br>
   √ Would you like to customize the import alias (`@/*` by default)? » <u>No</u> / Yes
   Creating a new Next.js app in `F:\e-commerce`.

   Using npm.

   Initializing project with template: app-tw


   Installing dependencies:<br>
   \- react<br>
   \- react-dom<br>
   \- next

   Installing devDependencies:<br>
   \- typescript<br>
   \- @types/node<br>
   \- @types/react<br>
   \- @types/react-dom<br>
   \- postcss<br>
   \- tailwindcss<br>
   \- eslint<br>
   \- eslint-config-next<br>
   \- @eslint/eslintrc<br>

   added 375 packages, and audited 376 packages in 26s

   144 packages are looking for funding<br>
   run `npm fund` for details

   found 0 vulnerabilities<br>
   Success! Created commerce at F:\e-commerce

2. Install components
   
   * User Interface

     ```sh
     # Add UI components
     npx shadcn@latest init
     npx shadcn@latest add alert-dialog
     npx shadcn@latest add badge
     npx shadcn@latest add button
     npx shadcn@latest add card
     npx shadcn@latest add carousel
     npx shadcn@latest add checkbox
     npx shadcn@latest add dialog
     npx shadcn@latest add drawer
     npx shadcn@latest add dropdown-menu
     npx shadcn@latest add form
     npx shadcn@latest add input
     npx shadcn@latest add label
     npx shadcn@latest add radio-group
     npx shadcn@latest add select
     npx shadcn@latest add sheet
     npx shadcn@latest add sonner
     npx shadcn@latest add table
     npx shadcn@latest add textarea
     npx shadcn@latest add toast
     ```

   * Packages
   
     ```sh
     npm i next-themes
     npm i @neondatabase/serverless @prisma/adapter-neon ws
     npm i -D @types/ws bufferutil
     npm i bcrypt-ts-edge
     npm i next-auth@beta --legacy-peer-deps
     npm i @auth/prisma-adapter
     # For variables NEXTAUTH_SECRET in .env file
     openssl rand -base64 32
     npm i -D jest ts-jest ts-node @types/jest @types/node dotenv --legacy-peer-deps
     npm init jest@latest
     ```

     √ Would you like to use Typescript for the configuration file? ... yes<br>
     √ Choose the test environment that will be used for testing » node<br>
     √ Do you want Jest to add coverage reports? ... no<br>
     √ Which provider should be used to instrument code for coverage? » v8
     √ Automatically clear mock calls, instances, contexts and results before every test? ... yes<br>

     📝  Configuration file created at F:\e-commerce\jest.config.ts

     ```sh
     npm i @paypal/react-paypal-js
     npm i @paypal/react-paypal-js --legacy-peer-deps
     npm i recharts --legacy-peer-deps
     npm i slugify
     npm i uploadthing @uploadthing/react --legacy-peer-deps
     npm i embla-carousel-autoplay embla-carousel-react
     npm i stripe @stripe/stripe-js @stripe/react-stripe-js --legacy-peer-deps
     npm i resend react-email @react-email/components --legacy-peer-deps
     npm i query-string
     ```

   * Databases (Postgres)
   
     ```sh
     npm i -D prisma @prisma/client
     npx prisma@latest init
     # Create the model under prisma/schema.prisma
     # Generate the migrations
     npx prisma generate
     npx prisma migrate dev --name init
     # View migrations database using tools
     npx prisma studio
     # Seed sample data into Vercel Postgres database
     npx tsx ./db/seed
     # After package dependencies for WebSocket was installed
     npx prisma generate
     # Authentication (Prisma)
     # https://authjs.dev/getting-started/adapters/prisma?framework=next-js
     
     # Seed model changes
     npx prisma generate
     npx prisma migrate dev --name add_user_based_tables

     # Seed users
     npx tsx ./db/seed
     ```
   
   * VS Code Extensions
   
     ```sh
     Prisma
     # Open User Preference (Ctrl + Shift + P)
     # Lookup for "Preferences: Open User Settings (JSON)"
     # Add entries at last
     "[prisma]": {
        "editor.defaultFormatter": "Prisma.prisma"
     }
     # Start Prisma model migrations
     Multiple cursor case preserve
     ```
   
   * Test
   
   ```sh
   npm test
   # Send email template preview
   # Visit http://localhost:3001
   npm run email
   ```

3. Start the application
   
   ```sh
   # Development
   npm run dev
   # Production
   npm run build
   ```

4. Push to Git Repository
   
   ```sh
   git init -b master
   git add .
   git commit -m 'Initial commit'
   git remote add http://
   git push -u origin master
   ```

5. Vercel Cloud Deployment
   
   Framework Preset

   ```
   Next.js
   ```

   Root Directory

   ```
   ./
   ```

   Build and Output Settings

   * Install Command

     ```sh
     npm install --legacy-peer-deps
     ```

   Environment Variables

   ```
   NEXT_PUBLIC_APP_NAME: Prostore
   NEXT_PUBLIC_APP_DESCRIPTION: A modern ecommerce store built with Next.js
   # NEXT_PUBLIC_SERVER_URL: http://localhost:3000
   NEXT_PUBLIC_SERVER_URL: https://prostore-one.vercel.app
   DATABASE_URL=postgres://neondb_owner:npg_GJcXLk8fP6iw@ep-hidden-shadow-a1q2j78y-pooler.ap-southeast-1.aws.neon.tech/neondb?sslmode=require
   NEXTAUTH_URL_INTERNAL: http://localhost:3000
   NEXTAUTH_URL: http://localhost:3000
   NEXTAUTH_SECRET: 
   NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY: 
   STRIPE_SECRET_KEY: 
   STRIPE_WEBHOOK_SECRET: 
   ```

   Finally, click 'Deploy' button. After successful deployment, click on 'Continue to Dashboard'

## Usage

### Install Dependencies

```bash
npm install
```

Note: Some dependencies may have not yet been upadated to support React 19. If you get any errors about depencency compatability, run the following:

```bash
npm install --legacy-peer-deps
```

### Environment Variables

Rename the `.example-env` file to `.env` and add the following

#### PostgreSQL Database URL

Sign up for a free PostgreSQL database through Vercel. Log into Vercel and click on "Storage" and create a new Postgres database. Then add the URL.

**Example:**

```
DATABASE_URL="postgresql://username:password@host:port/dbname"
```

#### Next Auth Secret

Generate a secret with the following command and add it to your `.env`:

```bash
openssl rand -base64 32
```

**Example:**

```
NEXTAUTH_SECRET="xmVpackzg9sdkEPzJsdGse3dskUY+4ni2quxvoK6Go="
```

#### PayPal Client ID and Secret

Create a PayPal developer account and create a new app to get the client ID and secret.

**Example:**

```
PAYPAL_CLIENT_ID="AeFIdonfA_dW_ncys8G4LiECWBI9442IT_kRV15crlmMApC6zpb5Nsd7zlxj7UWJ5FRZtx"
PAYPAL_APP_SECRET="REdG53DEeX_ShoPawzM4vQHCYy0a554G3xXmzSxFCDcSofBBTq9VRqjs6xsNVBcbjqz--HiiGoiV"
```

#### Stripe Publishable and Secret Key

Create a Stripe account and get the publishable and secret key.

**Example:**

```
STRIPE_SECRET_KEY="sk_test_51QIr0IG87GyTererxmXxEeqV6wuzbmC0TpkRzabxqy3P4BpzpzDqnQaC1lZhmYg6IfNarnvpnbjjw5dsBq4afd0FXkeDriR"
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY="pk_test_51QIr0Ids7GyT6H7X6R5GoEA68lYDcbcC94VU0U02SMkrrrYZT2CgSMZ1h22udb5Rg1AuonXyjmAQZESLLj100W3VGVwze"
```

#### Uploadthing Settings

Sign up for an account at https://uploadthing.com/ and get the token, secret and app ID.

**Example:**

```
UPLOADTHING_TOKEN='tyJhcGlLZXkiOiJza19saXZlXzQ4YTE2ZjhiMDE5YmFiOgrgOWQ4MmYxMGQxZGU2NTM3YzlkZGI3YjNiZDk3MmRhNGZmNGMwMmJlOWI2Y2Q0N2UiLCJhcHBJZCI6InRyejZ2NHczNzUiLCJyZWdpb25zIjpbInNlYTEiXX0='
UPLOADTHIUG_SECRET='gg'
UPLOADTHING_APPID='trz6vd475'
```

#### Resend API Key

Sign up for an account at https://resend.io/ and get the API key.

**Example:**

```
RESEND_API_KEY="re_ZnhUfrjR_QD2cDqdee3iYCrkfvPYFCYiXm"
```

### Run

```bash

# Run in development mode
npm run dev

# Build for production
npm run build

# Run in production mode
npm start

# Export static site
npm run export
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

## Prisma Studio

To open Prisma Studio, run the following command:

```bash
npx prisma studio
```

## Seed Database

To seed the database with sample data, run the following command:

```bash
npx tsx ./db/seed
```

## Demo

I am not sure how long I will have this demo up but you can view it here:

[ https://prostore-one.vercel.app/ ](https://prostore-one.vercel.app/)

## Bug Fixes And Course FAQ

### Fix: Edge Function Middleware Limitations on Vercel

After deploying your app you may be getting a build error along the lines of:

> The Edge Function "middleware size is 1.03 MB and your plan size limit is 1MB

For the solution to resolve this please see Brads [Gist here](https://gist.github.com/bradtraversy/16e3c89b9b25bc79cf86f5f36e14e83d)

There is also a new lesson added for this fix at the end of the course -
**Vercel Hobby Tier Fix**

### Bug: A newly logged in user can inherit the previous users cart

If a logged in user adds items to their cart and logs out then a different user
logs in on the same machine, they will inherit the first users cart.

To fix this we can delete the current users **Cart** from the database in our **lib/actions/user.actions.ts** `signOutUser` action.

> Changes can be seen in [lib/actions/user.actions.ts](https://github.com/bradtraversy/prostore/blob/a498d4362d1485b2bd3152124cb5c3a75f8fdd70/lib/actions/user.actions.ts#L45)

### Bug: Any user can see another users order

If a user knows the `Order.id` of another users order it is possible for them to
visit **/order/<Order.id>** and see that other users order. This isn't likely to
happen in reality but should be something we protect against by redirecting the
user to our **/unauthorized** page if they are not the owner of the order.

In **app/(root)/order/[id]/page.tsx** we can import the `redirect` function from Next:

```ts
import { notFound, redirect } from 'next/navigation';
```

Then check if the user is the owner of the order and redirect them if not:

```ts
// Redirect the user if they don't own the order
if (order.userId !== session?.user.id) {
  return redirect('/unauthorized');
}
```

> Changes can be seen in [app/(root)/order/[id]/page.tsx](<https://github.com/bradtraversy/prostore/blob/main/app/(root)/order/%5Bid%5D/page.tsx>)
