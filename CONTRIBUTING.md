# Cosmos SDK Tutorials repo

This repo contains the code and content for the published [Cosmos SDK Tutorials](https://tutorials.cosmos.network/).

## Tutorials are version-specific

The code and the docs for each tutorial are based on a specific version of the software. Be sure to download and use the right version.

## Contributing

Thank you for helping us to create and maintain awesome tutorials.

- To set up your environment for success, you can follow our [technical set up](TECHNICAL-SETUP.md) guidelines.
- To provide feedback, file an issue and provide abundant details to help us understand how we can make it better.
- To provide feedback and a fix, you can make a direct contribution. This repo is protected since we provide the code and the docs to help you learn. If you're not a member or maintainer, fork the repo and then submit a PR from your forked repo to master.

## Metadata

The layout metadata at the top of the README.md file controls how the tutorial page is published. Write permissions are limited to preserve the structure and contents.

## Folder structure

Each Cosmos SDK tutorial lives in a self-describing folder: `blog`, `hello-world`, `voter`, and so on.

Two sub-folders are present for each production-ready tutorial:

- A self-describing sub-folder for the app and the rest of the code that runs the tutorial.
- A `tutorial` sub-folder for the Markdown files (*.md) that build the published tutorial docs.

Work-in-process tutorials might have content and code in other repos.

## Who works on the tutorials?

- The Tendermint (All in Bits) DevX team (@fadeev, @lubtd, @ilgooz and other amazing devs that I don't know the GitHub usernames for) develops the tutorial code and dependencies. Don't they do an amazing job?

- The Tendermint (All in Bits) EcoDev Engineering team (@toschdev, @lukitsbrian, @barriebyron) manages developer experience and owns the tutorial doc content.

- The Tendermint (All in Bits) Design team owns the front end and publishing. Be sure to check with @lovincyrus for details about the metadata for layout and publishing tutorials.

## Viewing Tutorial Builds

There are two ways to see what your changes will look like in production before the updated pages are published. 

- When a PR is ready for review, you can see a deployed preview on a URL that is unique for that PR.
- While a PR is in DRAFT mode, you can preview a local build.

### Preview PRs on a Deployed Preview 

After the PR moves from **Draft** to **Ready for review**, the CI status checks generate a Netlify deploy preview. Netlify keeps this preview up to date as you continue to work and commit new changes to the same branch.

To view a deployed preview on a **Ready for review** PR, click the **Details** link on the netlify commit status line:

![deploy-preview](./deploy-preview.png)

### Preview Draft PRs on a Local Web Browser

Since the deploy preview doesn't work on Draft PRs, follow these steps to preview the tutorial build on a local web browser.

1. If you haven't already, clone the tutorials repo to your local machine and change to that directory. For example:

  ```
  cd ~/github
  git clone https://github.com/cosmos/sdk-tutorials
  cd sdk-tutorials
  ```

2. Local tutorials require JavaScript. If needed, install [npm](https://docs.npmjs.com/cli/v6/commands/npm-install).

3. For each branch you work in, install the npm packages for the SDK tutorials:

  ```
  npm install
  ```

4. Start the local instance of the tutorial build:

  ```
  npm run serve
  ```

  A successful client compile looks like: `> VuePress dev server listening at http://localhost:8080/ ✔ Client Compiled successfully in 280.71ms success [12:06:28] Build 03d41f finished in 283 ms! ( http://localhost:8080/ )`

5. You can now view the tutorial build on a local web browser. Isn't this fun?

  Tip: On a mac, press the command key and click `http://localhost:8080/` for quick access.