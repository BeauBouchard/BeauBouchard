<p><a href="/">home</a> / <a href="/guides">guides</a></p>
<div class="rainbow-retro"></div>

# Make a Collapsible in Markdown

## Simple Usage

### A collapsible Details Section Containing markdown

<details>
  <summary>Click to expand!</summary>

  <h2>Heading</h2>

  <ol>
    <li>both numbered</li>
    <li>and lettered ordered lists</li>
    <li>and unordered lists
      <ul>
        <li>with bullets</li>
        <li>or sub-bullets</li>
      </ul>
    </li>
  </ol>

</details>

### Structure in Markdown

```
### A collapsible Details Section Containing markdown

<details>
  <summary>Click to expand!</summary>
  
  ## Heading
  1. both numbered
  2. and lettered ordered lists
  3. and unordered lists
     * with bullets
     * or sub-bullets
</details>

```

<p class="spacers"> </p>

### Structure in HTML / Githubpages

```
### A collapsible Details Section Containing markdown

<details>
  <summary>Click to expand!</summary>

  <h2>Heading</h2>

  <ol>
    <li>both numbered</li>
    <li>and lettered ordered lists</li>
    <li>and unordered lists
      <ul>
        <li>with bullets</li>
        <li>or sub-bullets</li>
      </ul>
    </li>
  </ol>

</details>

```

<p class="spacers"> </p>

# NOTE:

<p class="spacers"> </p>

## Very important rules for github markdown

<p class="spacers"> </p>

1. **MUST HAVE** an **empty line** after the closing `</summary>` tag.
2. **MUST HAVE** an **empty line** after the closing `</details>` tag if you have multiple collapsible sections.
3. **FOR** Github Pages, all content inside of HTML tags **MUST BE** in HTML, not markdown. 

otherwise the markdown/code blocks won't show correctly.

<p class="spacers"> </p>

## Advanced Usage

