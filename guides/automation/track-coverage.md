<p><a href="/">home</a> / <a href="/guides">guides</a></p>
<div class="rainbow-retro"></div>

# Add Code Coverage Tracking to your Repo with CodeCov

This is the third part in a series about making github actions, make sure to check out the rest of them

 - <a href="/guides/automation/github-actions">Github Actions Primer</a>
 -  - <a href="/guides/automation/github-actions">Linting</a>
 -  - <a href="/guides/automation/github-actions">Testing</a>
 -  - <a href="/guides/automation/track-coverage">Code Coverage</a>

## Making a Github Action

As we previously have made a `.github/workflows/push.yml`, where it installs and tests code, we are creating a new task called `codecoverage` which will setup a new `ubuntu` environment, securly checkout he code, install npm and all the dependancies. 

The last two steps we are adding which are unique in this document are to use `jest` to generate a codecoverage output folder, which we then upload to CodeCov, a codecoverage SASS provider for tracking your codecoverage overtime for your repos. 

```yaml
  - name: CodeCoverage Generation . . .
    run: npm run test:coverage
  - name: Uploading to Codecov . . .
    uses: codecov/codecov-action@v2
    with:
      token: ${{ secrets.CODECOV_TOKEN}} # not required for public repos
      # fail_ci_if_error: true # optional (default = false)
      verbose: true # optional (default = false)
```


For instructions about setting up a codecov account, checkout this document on their site here. 

Which all starts by setting up a repo with an <a href="https://about.codecov.io/sign-up/">account from github here</a>. 


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
      - name: CodeCoverage Generation . . .
        run: npm run test:coverage
      - name: Uploading to Codecov . . .
        uses: codecov/codecov-action@v2
        with:
          token: ${{ secrets.CODECOV_TOKEN}} # not required for public repos
          # fail_ci_if_error: true # optional (default = false)
          verbose: true # optional (default = false)
```



### Read More!

 * <a href="https://github.com/codecov/codecov-action">Read more about codecov/codecov-action@v2 here</a>

<p class="spacers"> <br /></p>
<div align="center" >
  <p>
    <a href="https://beau.sh/guides/">⬅️ Back to Guides</a>
  </p>
</div>
