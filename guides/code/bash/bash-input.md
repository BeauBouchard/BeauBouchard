
<p><a href="/">home</a> / <a href="/guides">guides</a></p>
<div class="rainbow-retro"></div>

<h1>Input for your Bash Scripts</h1>


<p>A function I have been using in my bash scripts allows me to collect user input in a very simple way.</p>

```bash
  port=$(input_user  "what port for server?" 8080)
```

<p>Which will prompt the user for a text input, but also have the option for a default answer. </p>

<p>The function looks like this . . .</p>

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

## Detailed Explaination


Using the `read -p` command above means you want to execute `read` using the `-p` option, which stands for prompt.
	
<p><a href="https://ss64.com/bash/read.html">-p (prompt)</a> - Display prompt on standard error, without a trailing newline, before attempting to read any input. The prompt is displayed only if input is coming from a terminal.</p>


<p><a href="https://tldp.org/LDP/Bash-Beginners-Guide/html/sect_07_01.html">If</a> checks the return string of the input function, using a string comparison. But there are many other things you can do with responses.</p>


<p class="spacers"> <br /></p>
<div align="center" >
  <p>
    <a href="https://beau.sh/guides/#bash">More Bash Guides . . .</a>
  </p>
  <p>
    <a href="https://beau.sh/guides/">⬅️ Back to Guides</a>
  </p>
</div>
