
<p><a href="/">home</a> / <a href="/guides">guides</a></p>
<div class="rainbow-retro"></div>

# Itterate through a JSON file in Bash


Assume that you have a file of people, this file called "people.json", which looks something like this . . .

```JSON
[
  {"name":"Bob","favorite_color":"red"},
  {"name":"Doug","favorite_color":"blue"},
  {"name":"Samantha","favorite_color":"red"},
  {"name":"Jessica","favorite_color":"green"},
]

```

Now, you may want to itterate on each of those json objects to get the values of each. 

This is easy to do with the "jq" command like the following: 

```bash
read_json() {
	while IFS= read -r NAME && IFS= read -r FAVCOLOR; do
    echo "${NAME}'s favorite color is ${FAVCOLOR}"
  done < <(jq -r ".[] | .name, .favorite_color" ./people.json)
}
```

The output of the above command should look like this: 

```bash
Bob's favorite color is red
Doug's favorite color is blue
Samantha's favorite color is red
Jessica's favorite color is green
```

## Detailed Explaination


<p class="spacers"> <br /></p>
<div align="center" >
  <p>
    <a href="https://beau.sh/guides/">⬅️ Back to Guides</a>
  </p>
</div>
