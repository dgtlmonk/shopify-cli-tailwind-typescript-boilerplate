# Perkd Membership Shopify

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE.md)
[![Build Status](https://travis-ci.com/Shopify/shopify-app-node.svg?branch=master)](https://travis-ci.com/Shopify/shopify-app-node)

Boilerplate to create an embedded Shopify app made with Node, [Next.js](https://nextjs.org/), [Shopify-koa-auth](https://github.com/Shopify/quilt/tree/master/packages/koa-shopify-auth), [Polaris](https://github.com/Shopify/polaris-react), and [App Bridge React](https://shopify.dev/tools/app-bridge/react-components).

## Setting up

Make sure that you first complete these setup instructions:

1. [Install the latest stable version of Node.js.](https://developers.shopify.com/tutorials/build-a-shopify-app-with-node-and-react/set-up-your-app#install-the-latest-stable-version)
2. Install npm packages (run: npm install).
3. [Expose your dev environment.](https://developers.shopify.com/tutorials/build-a-shopify-app-with-node-and-react/embed-your-app-in-shopify#expose-your-dev-environment)
4. [Get a Shopify API key and Shopify API secret key.](https://developers.shopify.com/tutorials/build-a-shopify-app-with-node-and-react/embed-your-app-in-shopify#get-a-shopify-api-key)
5. [Add the Shopify API key and Shopify API secret key.](https://developers.shopify.com/tutorials/build-a-shopify-app-with-node-and-react/embed-your-app-in-shopify#add-the-shopify-api-key)
6. Add `HOST='http://{your_forwarding_id}.ngrok.io'`
7. Start your app (run: npm run dev).
8. [Authenticate and test your app.](https://developers.shopify.com/tutorials/build-a-shopify-app-with-node-and-react/embed-your-app-in-shopify#authenticate-and-test)
9. [Set up your app navigation.](https://developers.shopify.com/tutorials/build-a-shopify-app-with-node-and-react/build-your-user-interface-with-polaris#set-up-your-app-navigation)
10. [Add your ngrok url as Host.](https://developers.shopify.com/tutorials/build-a-shopify-app-with-node-and-react/charge-a-fee-using-the-billing-api#set-up)

### Local Development

```sh
npm run dev
```

### Tunnel via Ngrok server

```sh
ngrok http -subdomain=perkd-dev 8081
```

## Environment Setup

In your .env.local file

```
SHOP={your_shop.shopify.com}
HOST={your_tunnel_host}
```

## Shop Installation

```sh
https://perkd-dev.ngrok.io/auth?shop={your-shop-name}.myshopify.com
```

## Requirements

- If you don’t have one, [create a Shopify partner account](https://partners.shopify.com/signup).
- If you don’t have one, [create a Development store](https://help.shopify.com/en/partners/dashboard/development-stores#create-a-development-store) where you can install and test your app.
- In the Partner dashboard, [create a new app](https://help.shopify.com/en/api/tools/partner-dashboard/your-apps#create-a-new-app). You’ll need this app’s API credentials during the setup process.

## Coding Guidelines

**FRONTEND DEVELOPMENT PHILOSOPHY**

> Don't sacrifice readability for 'performance' unless there's evidence that this is a hot path

### Make it Run, Make it Right, Make it fast. - THE ITERATION PHASE

https://wiki.c2.com/?MakeItWorkMakeItRightMakeItFast

1. Meet the minimum requirements for the business to call the project a success. (`Make it work.`)
2. Add bells and whistles to make the program less prone to error and more feature-rich. (`Make it right.`)
3. Find and eliminate waste in the process. Some assumptions from the start will have been incorrect. Remove unnecessary business logic. Included in this step is to improve code for better performance. (`Make it fast.`)

---

## Conventional Commits

### A specification for adding human and machine-readable meaning to commit messages

semantic commit messages. e.g.:

```
feat: add login page
^--^ ^------------^
| |
| +-> Summary in present tense.
|
+-------> Type: chore, docs, feat, fix, refactor, style, or test.
```

`feat`: (new feature for the user, not a new feature for build script) </br>
`fix`: (bug fix for the user, not a fix to a build script) <br />
`docs`: (changes to the documentation) <br />
`style`: (formatting, missing semi colons, etc; no production code change) <br />
`refactor`: (refactoring production code, eg. renaming a variable) <br />
`test`: (adding missing tests, refactoring tests; no production code change) <br />
`chore`: (updating grunt tasks etc; no production code change)<br />

### References:

[Conventional Commits](https://www.conventionalcommits.org/) <br />
[Semantic Commits](https://seesparkbox.com/foundry/semantic_commit_messages) <br />
[Git Commit Msg](http://karma-runner.github.io/1.0/dev/git-commit-msg.html) <br />

## License

This repository is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).
