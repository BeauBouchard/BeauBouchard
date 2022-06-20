<p><a href="/">home</a> / <a href="/guides">guides</a></p>
<div class="rainbow-retro"></div>

# Adding Quick Github Actions to Automate things!

Adding automation is not just for production, you should be adding them to all your environments. in this short guide you will add several types of Github actions to a workflow. 

Github actions are infrastructure as code, and are created in YAML declarations that exist in the repo. 

Start by creating a new file in you repo, `.github/workflows/push.yml`

YAML uses tabs to determine the scope, so make sure you format your file as such:

```yaml
name: Default Node CI

on:
  pull_request:
    types: [opened, synchronize, reopened]

```



## Code Linting!

```yaml
name: Default Node CI

on:
  pull_request:
    types: [opened, synchronize, reopened]
    
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

## Code Testing!

```yaml

```

## Code Coverage!



## Code Quality!

## Advanced Usage

### Read More!

 * <a href="">Read more about Github Actions on their Documentaiton Page</a>

<p class="spacers"> <br /></p>
<div align="center" >
  <p>
    <a href="https://beau.sh/guides/">⬅️ Back to Guides</a>
  </p>
</div>
