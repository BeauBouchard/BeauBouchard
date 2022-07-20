<p><a href="/">home</a> / <a href="/guides">guides</a></p>
<div class="rainbow-retro"></div>

# Github Actions Primer

### Adding Quick Github Actions to Automate things!

 - <a href="/guides/automation/github-actions">Github Actions Primer</a>
   -  <a href="/guides/automation/github-actions-linting">Linting</a>
   -  <a href="/guides/automation/github-actions-testing">Testing</a>
   -  <a href="/guides/automation/github-actions-track-coverage">Code Coverage</a>

Adding automation is not just for production, you should be adding them to all your environments. In this short guide you will add several types of Github actions to a workflow. 

Github actions are infrastructure as code, and are created in YAML declarations that exist in the repo. 

Start by creating a new file in you repo, `.github/workflows/push.yml`

YAML uses tabs to determine the scope, so make sure you format your file as such:

```yaml
name: Default Node CI

on:
  pull_request:
    types: [opened, synchronize, reopened]

```

## Linting 

   -  <a href="/guides/automation/github-actions-linting">Linting</a>

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
