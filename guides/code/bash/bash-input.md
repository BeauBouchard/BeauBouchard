
<p><a href="/">home</a> / <a href="/guides">guides</a></p>
<div class="rainbow-retro"></div>

<h1>Input for your Bash Scripts</h1>


<p>A function I have been using in my bash scripts allows me to collect user input in a very simple way.</p>

```bash
  port=$(input_user  "what port for server?" 8080)
```

which will prompt the user for a text input, but also have the option for a default answer. 

The function looks like this

```bash
# input decision for user, useful for assigning variiable values
# usage: prompt_user <prompt message> [fallback value*]
#   * uses fallback/default value if no input recieved
# example:
#   name=$(input_user  "what is your name?")
#   port=$(input_user  "what port for server?" 8080)
input_user() {
  local input=
  # set text prompt value
  local prompt="${1:-value}"
  # set default value
  local default="$2"
  [ -z "$default" ] || prompt+=" [$default]"

  # convert escape sequences in prompt to ansi codes
  prompt="$(echo -en "$prompt : ")"

  while [ -z "$input" ]; do
    if [ -t 0 ]; then
      # user input
      read -p "$prompt" input </dev/tty
    else
      # piped input
      read input
    fi

    [[ -n "$default" && -z "$input" ]] && input="$default"
    [ -z "$input" ] && echo -en "invalid input"

  done
  echo "$input"
}
```

<p>You can even read back that value into a variable which you can check. Which allows you to do more complex interactions from your bash commands, set options and allow them to be more robust. Here is the same function being used to read a simple choice... </p>

```bash
# Asks the user "yes" or "no" 
delete_check() {
  ANSWER=$(input_user  "Are you sure you want to Delete this?" no)
	if [ "$ANSWER" == "yes" ]; then
			echo -en "deleting this . . .";
	elif [ "$ANSWER" == "no" ]; then
			echo -en "Exiting without Deleting . . .";
	else
			echo -en "Invalid Input, Answer 'yes' or 'no'";
	fi
  return 0;
}
```


<p class="spacers"> <br /></p>
<div align="center" >
  <p>
    <a href="https://beau.sh/guides/">⬅️ Back to Guides</a>
  </p>
</div>
