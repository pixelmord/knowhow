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