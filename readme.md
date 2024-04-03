#Passos 

#1 Open a Terminal in Linux/Macos (or a Command Prompt in Windows)
Issue the commands to create a new folder to contain our project

mkdir first-ts-repo
cd first-ts-repo

#2 Issue the command to initialize a npm package
npm init -y

    Notes:
    npm is a package manager for the JavaScript programming language. It is the
    default package manager for the JavaScript runtime environment Node.js
    It is used to manage the dependencies that our project has on other packages
    A package is a unit of software distribution (i.e., a library of code)
    The command will create a new file in the folder called package.json. We will want
    to commit this file into our repository

#3 npm install typescript --save-dev
    Notes:
    npm install instructs npm to add a new dependency to our project, in this case
    typescript
    The option –save-dev allows to save packages under the devDependencies object in
    the package. json file
    Typescript is a dependency only used during development
    The command will update the file package.json. Also a new file named
    package-lock.json should be present in the folder. We will want to commit this file
    into our repository
    package-lock.json is automatically generated for any operations where npm modifies
    either the node_modules tree, or package.json. It describes the exact tree that was
    generated, such that subsequent installs are able to generate identical trees, regardless
    of intermediate dependency updates.
    This command will create a folder named node_modules that is used to contain the
    dependent packages. We do not want to commit this folder into our repository. It
    should be ignored.

#4 npm install @types/node --save-dev

#5 npx tsc --init --rootDir src --outDir build --esModuleInterop --resolveJsonModule --lib es6 --module commonjs --allowJs true --noImplicitAny true 

#6 console.log("Ola mundo");

#7 npx tsc

#8 node build/app.js