
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

```
Bob's favorite color is red
Doug's favorite color is blue
Samantha's favorite color is red
Jessica's favorite color is green
```

## Detailed Explaination

<p>Using the raw output from JQ, we can then itterate over every json as if it was an entry from an array. Then using the named pipes, we can name the Inputs for the READ command.</p>
<p><strong>--raw-output / -r:</strong> - With this option, if the filter's result is a string then it will be written directly to standard output rather than being formatted as a JSON string with quotes. This can be useful for making jq filters talk to non-JSON-based systems. -- <a href="https://stedolan.github.io/jq/manual/">jq man pages</a></p>
<p>While we are looping, the the <strong>-r</strong> option on <strong>read</strong> prevents it from treating backslash as a special character. -- <a href="https://ss64.com/bash/read.html">man for bash / read</a></p>



<p class="spacers"> <br /></p>
<div align="center" >
  <p>
    <a href="https://beau.sh/guides/">⬅️ Back to Guides</a>
  </p>
</div>
