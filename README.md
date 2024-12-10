# Try T3 App

This is a [T3 Stack](https://create.t3.gg/) project bootstrapped with `create-t3-app`.

Deployed to https://try-t3-app.linwise.com/

Followed the [T3 Stack](https://create.t3.gg/) guide and added discord login.

## Notes

- Added `NEXTAUTH_URL` to make sure the correct callback URL is used.
- Added `AUTH_TRUST_HOST` according to [auth.js docs](https://authjs.dev/getting-started/deployment#auth_trust_host).

  Compared to the original project, I have added the following in `.env` file:

  ```ini
  NEXTAUTH_URL=http://localhost:3000 # local development
  # NEXTAUTH_URL=https://try-t3-app.linwise.com/ # production

  AUTH_TRUST_HOST="localhost" # local development
  # AUTH_TRUST_HOST="try-t3-app.linwise.com" # production
  ```

- Added these redirect urls in discord developer portal:

  ```plain
  http://localhost/api/auth/callback/discord
  https://try-t3-app.linwise.com/api/auth/callback/discord
  ```

## Links

- https://create.t3.gg/en/usage/first-steps
- https://create.t3.gg/en/introduction

## What's next? How do I make an app with this?

We try to keep this project as simple as possible, so you can start with just the scaffolding we set up for you, and add additional things later when they become necessary.

If you are not familiar with the different technologies used in this project, please refer to the respective docs. If you still are in the wind, please join our [Discord](https://t3.gg/discord) and ask for help.

- [Next.js](https://nextjs.org)
- [NextAuth.js](https://next-auth.js.org)
- [Prisma](https://prisma.io)
- [Drizzle](https://orm.drizzle.team)
- [Tailwind CSS](https://tailwindcss.com)
- [tRPC](https://trpc.io)

## Learn More

To learn more about the [T3 Stack](https://create.t3.gg/), take a look at the following resources:

- [Documentation](https://create.t3.gg/)
- [Learn the T3 Stack](https://create.t3.gg/en/faq#what-learning-resources-are-currently-available) — Check out these awesome tutorials

You can check out the [create-t3-app GitHub repository](https://github.com/t3-oss/create-t3-app) — your feedback and contributions are welcome!

## How do I deploy this?

Follow our deployment guides for [Vercel](https://create.t3.gg/en/deployment/vercel), [Netlify](https://create.t3.gg/en/deployment/netlify) and [Docker](https://create.t3.gg/en/deployment/docker) for more information.
