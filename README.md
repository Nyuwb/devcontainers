# Dev Containers collection

## What is this repository ?

It's a collection of Visual Studio Code Dev Containers that I'm using at work or on personal projects.   
Feel free to fork this repository to use them on your side and adapt the content for your need.

## How is the repository organized ?

A directory is dedicated to a language/tech.  
Sometimes there are more than one container in the directory, for example `php+mysql` will build two containers, one for `php` and one for `mysql`.

## How can I download only one subdirectory in my project ?

Here is a short example with the `php` subdirectory :

```bash
# Clone the directory without downloading any file in a temporary directory
git clone -n --depth=1 --filter=tree:0 https://github.com/Nyuwb/devcontainers.git temp-devcontainer
cd temp-devcontainer

# Limit the checkout to the wanted subdirectory
git sparse-checkout set --no-cone php
git checkout

# Move the downloaded subdirectory to .devcontainer and remove the temporary created directory
cd ../
mv temp-devcontainer/php .devcontainer
rm -rf temp-devcontainer
```

## The devcontainer is not working on my side, what can I do ?

If you are using WSL, please check/update your version.  
Otherwise, just read the logs from VS Code to see what's wrong.
