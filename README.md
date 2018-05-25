# JavaScript Development Environment

This is a generic JavaScript development environment 
This isn't tied to any specific JS framework.

## Get Started

1. **Install node
2. **Install yarn
4. **Install Node Packages.** - `yarn install`
5. **Run the app.** - `yarn start -s`
This will run the automated build process, start up a webserver, and open the application in your default browser.
When doing development with this kit, this command will continue watching files all your files. Every time you hit save the code is rebuilt, linting runs, and tests run automatically.
Note: The -s flag is optional. It enables silent mode which suppresses unnecessary messages during the build.
6. Having issues? See below.

## Having Issues? Try these things first:

1. Run `yarn install` - If you forget to do this, you'll see this: `babel-node: command not found`.
2. Make sure you're running the latest version of Node. N.B. Node 7 has issues on some Windows machines.
3. Make sure files with names that begin with a dot (.babelrc, .editorconfig, .eslintrc) are copied to the project directory root. This is easy to overlook if you copy this repository manually.
4. Don't run the project from a symbolic link. It will cause issues with file watches.
5. Having linting issues? Delete any .eslintrc that you're storing in your user directory. Also, disable any ESLint plugin / custom rules that you've enabled within your editor.
6. Nothing above work? Delete your node_modules folder and re-run yarn install.

## Why CI server

The tipical developer answer: "It works on my machine!?"

- Forgot to commit new file
- Forgot to update package.json
- Commit doesn't run cross-platform
- Node version conflicts
- Bad Merge
- Pushed without running tests

### A CI server catches mistaches quickly. Because:

- Run automated build
- Run tests
- Check code coverage
- Automate deployment

### Some Options for CI servers

- Travic   (runs on Linux)
- Appveyor (runs on Windows)
- Jenkins
- CirleCI
- Semaphore
- SnapCI
