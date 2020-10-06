# Coding Guidelines
These guidelines aim to have a good and standardized way to write and commit code.

* [Coding Python](#coding-python)
  * [Module](#module)
* [Committing](#committing)
   * [Prerequisites](#prerequisites)
      * [(Optional) (macOS) Install brew](#optional-macos-install-brew)
      * [(Optional) Install npm](#optional-install-npm)
      * [Install Commitizen](#install-commitizen)
   * [Init project folder](#init-project-folder)
      * [Seamless](#seamless)
   * [Commit](#commit)



## Coding Python
### Module
Each tool created in the team has to be as a Python module: easy to install, easy to deploy. A skeleton is available at https://github.com/brsynth/module.

## Committing
Having good (browseable and readable) commits guarantees a reliable collaborative work in space and time. To address this topic, we use Commitizen to have standardized and readable commits in our projects.

### Prerequisites

#### (Optional) (macOS) Install brew
```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

#### (Optional) Install npm
- On macOS: `brew install npm`
- On Debian-like: `apt-get install npm`
- On Alpine-like: `apk add npm`

#### Install Commitizen
```sh
npm install commitizen -g
```

### Init project folder
```sh
npm init
commitizen init cz-conventional-changelog --save-dev --save-exact
```

#### Seamless
To avoid footprint in the project repository, add npm files into the `.gitignore` file:
```
package.json
package-lock.json
node_modules
```

### Commit
Replace your usual commit command (e.g. `git commit -am`) by:
```sh
git cz -am
```
