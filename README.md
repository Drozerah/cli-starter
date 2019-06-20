# CLI Starter

> A Command Line Interface starter boilerplate 

This material comes with the minimum settings and files that are required to start the creation of a new CLI utility with a Node.js and NPM environment.

## Structure
````
├───bin/
│   └───cli.js
├───.gitignore
├───licence
├───package-lock.json
├───package.json
└───README.md
````
## Install

````bash
$ git clone https://github.com/Drozerah/cli-starter.git
````
Then install globally: 
````bash
$ npm install -g
````
Once you are done with this step, you need to:

````bash
$ npm link
````
This command will register your CLI project locally so you are now able to run the command below anywhere into the terminal:

````bash
$ cli-starter
````
This command will prompt a message into the terminal meaning that everything is fine with the installation of _cli-starter_ module:

![cli starter](https://raw.githubusercontent.com/Drozerah/MyGitHubStorage/master/gif/cli-starter/cli-starter.gif)

__CLI command name:__

Because all projects are differents, you'll certainly need to change the name of the command that runs your own CLI:

`package.json`
```diff
{
//...
    "bin": {
-       "cli-starter": "bin/cli.js"
+       "myCommand": "bin/cli.js"
    }
//...
}
```

__Development:__ 

````bash
$ npm run dev
````
This command will execute the `cli-starter\bin\cli.js` JavaScript file, it can also be used during the development phase of your project...

__Notes:__

In order to prevent accidental publication of you project, the `"private"` key is set to `true` by default - to publish your project to the NPM registry you must turn the value to `false`

`package.json`
```diff
{
//...
-    "private": true
+    "private": false
//...
}
```

`npm command`

If you want or have to unregister your project, you'll need to unbind the symlink created from your project's directory to your global node modules, keep in mind to:
````bash
$ npm unlink
````
This command will also disable the `cli-starter` command into the terminal.

---------------

__Versioning__

- we use [SemVer](http://semver.org/) for versioning

__Author__

- Thomas G. aka Drozerah - [GitHub](https://github.com/Drozerah)

__License__

- [ISC](licence) © Thomas G. aka Drozerah



