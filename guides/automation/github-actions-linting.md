<p><a href="/">home</a> / <a href="/guides">guides</a></p>
<div class="rainbow-retro"></div>

# Add Linting to your CI with Github Actions

This is the First part in a series about making github actions, make sure to check out the rest of them

 - <a href="/guides/automation/github-actions">Github Actions Primer</a>
   -  <a href="/guides/automation/github-actions-linting">Linting</a>
   -  <a href="/guides/automation/github-actions-testing">Testing</a>
   -  <a href="/guides/automation/github-actions-track-coverage">Code Coverage</a>

## Making a Github Action for Linting

In this section we will focus on these three files to get our linter running. 
```
 ┣ 📂 .github
 ┃ ┗ 📂 workflows
 ┃   ┗ 📜 push.yml
 ┣ 📜.eslintrc.js
 ┗ 📜package.json
```

We covered in the main document about what starting a github-action with a file like `.github/workflows/push.yml` which start out with the 4 lines

```yaml
name: Default Node CI

on:
  pull_request:
    types: [opened, synchronize, reopened]
```

The last step we are adding which is unique in this document are to use `eslint`, our test runner, to test the code a code with our linter. 

```yaml
jobs:
  lint:
    name: lints
    runs-on: ubuntu-latest
    steps:
      - name: Checking Out Commits Securely . . .
        uses: actions/checkout@v2
      - name: Setup Node 14 Environment . . .
        uses: actions/setup-node@v1
        with:
          node-version: 14
      - name: Install Dependencies . . .
        working-directory: .
        run: npm ci
      - name: Run The Lints . . .
        run: npm run test:lint

```

In above for this example, we use the command `npm run test:lint` which corresponds to our `package.json` script `test:lint` which looks like this: 

```json
"scripts": {
 // ...
  "test": "jest",
  "test:watch": "jest --watchAll",
  "test:coverage": "jest --coverage | ./node_modules/.bin/codecov",
  "test:lint": "eslint . 'src/**/*.ts'",
  "test:lint:fix": "eslint . --fix 'src/**/*.ts'"
},
```

Our `.eslintrc.js` file for this project looks like so 

```js
module.exports = {
  parser: "@typescript-eslint/parser",
  plugins: [
    "@typescript-eslint",
    "prettier"
  ],
  extends: [
    "eslint:recommended",
    "plugin:@typescript-eslint/eslint-recommended",
    "plugin:@typescript-eslint/recommended",
    "prettier"
  ],
  rules: {
    "no-console": 1,       // Means warning
    "prettier/prettier": 2 // Means error
   },
  globals: {},
  ignorePatterns: ["**/*.js", "**/tests", "**/test"],
};

```


## Github Action YAML Standalone

If you  want here is the previously mentioned steps we covered

```yaml
name: Default Node CI

on:
  pull_request:
    types: [opened, synchronize, reopened]

jobs:
  codecoverage:
    name: codecoverage
    runs-on: ubuntu-latest
    steps:
      - name: Checking Out Commits Securely . . .
        uses: actions/checkout@v2
      - run: echo "💡 ${{ github.repository }} repo has been Cloned Successfully."
      - name: Setup Node 14 Environment . . .
        uses: actions/setup-node@v1
        with:
          node-version: 14
      - run: echo "🎉 Node 14 has been Installed Successfully."
      - name: Install Dependencies . . .
        working-directory: .
        run: npm ci
      - run: echo "🖥️ Deps Installed Successfully. The workflow is now ready!"
      - name: Run The Lints . . .
        run: npm run test:lint
```

As we previously have made a `.github/workflows/push.yml`, where it installs and tests code, we are creating a new task called `codecoverage` which will setup a new `ubuntu` environment, securly checkout he code, install npm and all the dependancies. 
