Update npm itself

npm install -g npm
#### Downgrade to a specific version
npm install -g npm@2
Check npm version

npm --version
Install a package

#### Local 
npm install package-name

#### Local + make an entry in package.json as dependency
npm install package-name --save

#### Install specific version of a package
npm install package-name@1.2.3

#### Global
npm install -g package-name
Un-install a package

#### Local
npm uninstall package-name

#### Global
npm uninstall package-name -g
Get package info

#### Home page
npm home package_name
#### Github repo
npm repo package_name
Check for outdated packages in package.json

#### Local
npm outdated

#### Global
npm outdated -g

#### Production only
npm outdated --prod
List installed packages

#### Local with tree
npm ls

#### Local - only parent
npm ls --depth=0

##### Global - only parent
npm ls -g --depth=0

#### List production packages only
npm ls --prod

Remove un-used packages from node_modules folder

npm prune

#### Remove all devDependencies from node_modules 
npm prune --production
Update all packages listed in package.json

npm update
Update a single package

npm update package_name
Remove duplicate packages from node_modules

npm dedupe
List packages in cache

npm cache ls
Clean npm cache

npm cache clean -f
💡 Bump version number in package.json and create a git tag automatically

npm version 1.2.3
Lockdown package versions for production

npm shrinkwrap
#### Also include devDependencies
npm shrinkwrap --dev
Run npm in production (will not download devDependencies)

npm install --only=production
Install a package from github

npm install git://github.com/user-name/package-name.git#v0.1.0
#### OR
npm install user/repo#v1.0.1
Install a package from local cache

npm install --cache-min 999999 package-name
View package info from its package.json file

npm view package_name property_in_json
npm install -g without sudo

mkdir ~/.npm-global
npm config set prefix '~/.npm-global'
chown -r user_name '~/.npm-global'
Some npm global configs

npm config set save-prefix ~
npm config set save-exact true
npm config set engine-strict true
npm config set ignore-scripts
npm config set init.author.name your_name  
npm config set init.author.email your_email  
Enable Auto completion

npm completion >> ~/.bashrc
Package.json extended docs
Package.json cheatsheet
Validate package.json
npm alternative - yarn
