# Coding Guidelines
These guidelines aim to have a good and standardized way to write and commit code.


## Committing
Having good (browseable and readable) commits guarantees a reliable collaborative work in space and time. To address this topic, we use Commitizen to have standardized and readable commits in our projects.

### Prerequisites

#### (Optional) (macOS) Install brew
On macOS:
```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

#### (Optional) Install npm
- On macOS:
```sh
brew install npm
```
- On Debian-like:
```sh
apt-get install npm
```
- On Alpine-like:
```sh
apk add npm
```

#### Install Commitizen
```sh
npm install commitizen -g
```

#### Init npm
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
```sh
git cz -am
```
