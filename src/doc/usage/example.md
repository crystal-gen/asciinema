```yaml
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