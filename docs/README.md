# KnowHow

A collection of things that are good to know ;)

## MacOS

### Clear caches

```bash
yarn cache clean
brew cleanup
# also remove latest versions of formulae
# brew  cleanup -s
# remove everything in homebrew cache (also downloads for installed versions)
# rm -rf $(brew --cache)
```

### SSH

```bash
# create key
ssh-keygen -t rsa -b 4096 -C "andreas.sahle@gmail.com"
# copy (default) public key to clipboard
pbcopy < ~/.ssh/id_rsa.pub
# add key to agent
ssh-add ~/.ssh/id_rsa
# list keys in agent
ssh-add -l
```

## Docker

```bash
# kill all running containers with
docker kill $(docker ps -q)
# delete all stopped containers with
docker rm $(docker ps -a -q)
# delete all images with
docker rmi $(docker images -q)

# list all running processes
docker ps -a
```

See also:
https://medium.com/the-code-review/top-10-docker-commands-you-cant-live-without-54fb6377f481

## Typescript

Book: https://basarat.gitbooks.io/typescript/

## VSCode

**Developers about their setups:**

May 20 '19
[dev.to/yloganathan/vs-code-setup-to-improve-developer-productivity-3die](https://dev.to/yloganathan/vs-code-setup-to-improve-developer-productivity-3die)

Feb 8 '19
[dev.to/vip3rousmango/vs-code-extensions-youll-actually-use-46gp](https://dev.to/vip3rousmango/vs-code-extensions-youll-actually-use-46gp)

Dec 25 '18
[dev.to/nickjj/my-favorite-vscode-extensions-and-settings-k5l](https://dev.to/nickjj/my-favorite-vscode-extensions-and-settings-k5l)

## Code Style

### Prettier

```js
  "prettier": {
    "singleQuote": true,
    "trailingComma": "es5",
    "printWidth": 80,
    "tabWidth": 2,
    "semi": true
  }
```

https://prettier.io/docs/en/options.html

https://prettier.io/docs/en/configuration.html

### Editorconfig

.editorconfig

```
# https://editorconfig.org
root = true

[*]
indent_style = space
indent_size = 2
end_of_line = lf
charset = utf-8
trim_trailing_whitespace = true
insert_final_newline = true

# Use 4 spaces for the Python files
[*.py]
indent_size = 4
max_line_length = 80

# The JSON files contain newlines inconsistently
[*.json]
insert_final_newline = ignore

# Minified JavaScript files shouldn't be changed
[**.min.js]
indent_style = ignore
insert_final_newline = ignore

# Makefiles always use tabs for indentation
[Makefile]
indent_style = tab

# Batch files use tabs for indentation
[*.bat]
indent_style = tab

[*.md]
trim_trailing_whitespace = false
```

https://editorconfig.org/