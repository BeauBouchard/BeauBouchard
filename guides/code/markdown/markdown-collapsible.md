<p><a href="/">home</a> / <a href="/guides">guides</a></p>
<div class="rainbow-retro"></div>

# Make a Collapsible in Markdown

## Simple Usage

### A collapsible Details Section Containing markdown

<details>
  <summary>Click to expand!</summary>
  
  ## Heading
  1. both numbered
  2. and lettered ordered lists
     * also with bullets
     * or Sub bullets
</details>

### Structure

```
### A collapsible Details Section Containing markdown

<details>
  <summary>Click to expand!</summary>
  
  ## Heading
  1. both numbered
  2. and lettered ordered lists
     * also with bullets
     * or Sub bullets
</details>

```

### A collapsible section containing code

<details>
  <summary>Click to expand!</summary>
  
  ```javascript
    function logger(message) {
      var date = new Date();
      console.log(`[${date.toISOString()}]: ${message}`);
    }
  ```
</details>

### Structure

```

### A collapsible section containing code

<details>
  <summary>Click to expand!</summary>
  
  ```javascript
    function logger(message) {
      var date = new Date();
      console.log(`[${date.toISOString()}]: ${message}`);
    }
  ```
</details>

```


# NOTE:
## Very important rules for github markdown

1. **MUST HAVE** an **empty line** after the closing `</summary>` tag.
2. **MUST HAVE** an **empty line** after the closing `</details>` tag if you have multiple collapsible sections.

otherwise the markdown/code blocks won't show correctly.


## Advanced Usage

