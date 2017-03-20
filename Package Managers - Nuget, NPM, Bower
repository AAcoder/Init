https://www.codeproject.com/Articles/1117120/NuGet-NPM-and-Bower

NuGet
it had lot of server side libraries, but you can get client libraries as well, But its main purpose is to distribute the server side libraries. Even Microsoft releases most of there libraries on NuGet nowadays, no need to download any package from website, just go to NuGet search for library and install.

Right click on project and select Manage NuGet Packages

What is it?   .Net developers are likely to be very familiar with this.  It is a package manager that mainly deals with .NET assemblies.
What it is good for?  It is nicely integrated within Visual Studio and great for loading .Net assemblies and libraries such as Entity Framework and ASP.NET Identity.


NPM (Node Package Manager)

npm is default package manager for Node.js. In old days only way to get java-script package was to get it from official website or CDN, most of them are still available to download from CDN and official website like Jquery and Angular. But if we have a common platform where we can get all libraries that will be great isn’t it. This is what npm does, it has all the java-script libraries.
Unlike NuGet it doesn’t comes with visual studio, you need to install node.js on your machine.You can download from here.

What is it?  Designed specifically for node modules, but is also ideal for loading packages that are used during development time. Unlike Bower, NPM supports nested dependency trees. Meaning, NPM may actually load multiple versions of a component on your machine.
What it is good for?  Great for managing developer tools like Yeoman, Grunt, Gulp, and testing tools. Its nested dependency tree makes it great for avoiding dependency conflicts.

Once node is installed let’s see how to use npm and install the package.

Once node is install go to command prompt, as i am working on windows you can run cmd.
Now change the current directory to your project , from command prompt change the directory.
Once you are on your project folder run node -v to check the current version of node,  
We don’t need to install npm as it comes with node.
To check the current version of npm run npm -v

Now check files in project, we will find an named package.json this is most important file here
Now let’s install the first package from npm, we will install typescript you can find all the packages from here.
Go to command prompt as fire 'npm install typescript' command. once command is executed open your package.json file. We will find a new changes dependencies added to our file. 
Hide   Copy Code
"dependencies": {},
  "devDependencies": {
    "copy-webpack-plugin": "^4.0.1",
    "source-map-loader": "^0.1.6",
    "ts-loader": "^2.0.1",
    "tslint": "^4.4.2",
    "typescript": "^2.2.1"
  }
  
Also we will see a folder “node_modules“ folder include the same. Notice we have typescript folder and required typescript libraries in it.


Bower

What is it?   Bower is optimized for front-end components. Bower uses a flat dependency tree, requiring only one version for each package, reducing page load to a minimum. So where NPM aims for stability, bower aims for a smaller/faster footprint.
What it is good for?  Created specifically for managing front-end components like javascript and css files.

Similar to npm and nuget, bower is one of the package manager, and like npm it is also a package manager for javascript. Confused when both are same, why to use bower, why npm is not enough.

npm is package manager where you can download the packages and use, but what if you want to keep track of packages which have new updates, download it automatically, in npm you can update the package when there is new update, but manually, bower does all these for you.No need to manually update the package.
So now we know the difference between npm and bower let’s see how it works.

Bower is an package which you can install from npm, it requires node,npm and git. For npm we have already installed node and npm comes with node, only thing left is git, you can download it from here.
Once git is installed, go to our command prompt and fire npm install -g bower to install bower.
Once bower is installed, fire bower init  to initialize bower for your current project.
like npm here also name is required parameter, once command is executed click on Show All Files, we will get bower.json file incude the same in your project.

Let’s install angular using the bower, fire bower install angular, once command is completed click on Show All Files again, we will see a new folder “bower_components” and it includes a folder called angular and files required for it.
In both package.json and bower.json file dependencies has all packages and its version name, if we want package to be referred only during development we can add a new tag dev-dependencies  and add the packages under it.
