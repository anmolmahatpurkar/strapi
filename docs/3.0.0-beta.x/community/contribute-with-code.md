# Contribute with Code

**NOTE:** All efforts to contribute are highly appreciated, we recommend you talk to a maintainer **prior** to spending a lot of time making a pull request that may not align with the project roadmap.

## Before Submitting a Pull Request

**Before submitting your pull request** make sure the following requirements are fulfilled:

- Fork the repository and create your branch from `master`.
- Run `yarn setup` in the repository root.
- If you’ve fixed a bug or added code that should be tested, add the tests and then link the corresponding issue in either your commit or your PR!
- Ensure the test suites are passing:
  - `yarn test:unit`
  - `yarn test:front`
- Make sure your code lints (`yarn lint`).
- When you write the Pull Request, please follow the [Pull Request Template](https://github.com/strapi/strapi/blob/master/.github/PULL_REQUEST_TEMPLATE.md)

## Technical Requirements

- You have [Node](https://nodejs.org/en/) at v10.x.x only and [Yarn](https://yarnpkg.com/en/) at v1.2.0+.
- You are familiar with Git, and have it installed on your development environment.

## Development Workflow

To facilitate the contribution, we have reduced the number of commands necessary to install the Strapi development environment.

First of all, you need to check if you're using the [required versions of Node.js and npm](/3.0.0-beta.x/getting-started/install-requirements.html)

Then, please follow the instructions below:

#### 1. ▪ Fork the [repository](https://github.com/strapi/strapi)

[Go to the repository](https://github.com/strapi/strapi) and fork it to your own GitHub account.

#### 2. 💿 Clone from your repository

```bash
git clone git@github.com:YOUR_USERNAME/strapi.git
```

#### 3. ⏳ Install the dependencies

Go to the root of the repository.

```bash
cd strapi && yarn setup
```

#### 4. 🚀 Start the example application

**Go to the getstarted application**

```bash
cd strapi/examples/getstarted
yarn develop
```

The server (API) is available at http://localhost:1337.

**Note:** Contributions involving the UI of any part of the administration panel, should complete the following step and take advantage of the additional tools.

**Start the administration panel server**

```bash
cd strapi/packages/strapi-admin
yarn develop
```

The administration panel is available at http://localhost:4000/admin

**Awesome! You are now able to contribute to Strapi.**

#### 5. Available commands

- `yarn watch` starts yarn watch in all packages.
- `yarn build` builds the `strapi-helper-plugin` (use this command when you develop in the administration panel).
- `yarn setup` installs the dependencies.
- `yarn lint` lints the codebase.
- `yarn test:clean` removes the coverage.
- `yarn test:front` runs the front-end related tests.
- `yarn test:front:watch` runs an interactive test watcher for the front-end.
- `yarn test:snyk` checks the dependencies vulnerabilities.
- `yarn test:unit` runs the back-end unit tests.
- `yarn test:e2e` runs an end-to-end test suite.
- `yarn test:generate-app` generates a test application.
- `yarn test:start-app` starts the test application.

---

## Running the tests

**Changing the database:**

You can run the test suites using different databases:

```bash
$ node test/e2e.js sqlite
$ node test/e2e.js mongo
$ node test/e2e.js postgres
$ node test/e2e.js mysql
```

---