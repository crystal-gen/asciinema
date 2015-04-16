# asciinema v0.1.0

[asciinema](http://asciinema.org) generator for [Crystal](http://crystal.sh)

# Schema

```yml
command:  # string
env:      # object
  shell:  # string
  term:   # string
duration: # number
height:   # number
stdout:   # array
  delay:  # number
  data:   # string
title:    # string
version:  # number
width:    # number
```

# Example

```yml
generators:
  asciinema:
    spec:
      command: /bin/zsh
      duration: 5
      env:
        term: screen-256color
        shell: /bin/zsh
      height: 24
      stdout:
        - data: ls
          delay: 0.4
        - data: .
        - data: ..
      title: asciinema test
      version: 1
      width: 80
    version: latest
```

# Output

```json
{
	"version": 1,
	"width": 80,
	"height": 24,
	"duration": 5,
	"command": "/bin/zsh",
	"title": "asciinema test",
	"env": {
		"TERM": "screen-256color",
		"SHELL": "/bin/zsh"
	},
	"stdout": [
		[
			0.4,
			"ls"
		],
		[
			1,
			"."
		],
		[
			1,
			".."
		]
	]
}
```