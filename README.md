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
- Codeship
- Solano

## Why Centralize API Calls

- Configure all calls
- Handle preloader logic
- Handle errors
- Single seam for mocking

## Why a mock server for API

What if we need a wide variety of data to build our app
and the services we need to call don't exisr yet?

- Unit Testing: Maybe you want to unit test your code so that your test run quickly and reliably, 
or maybe the existing web services in your development or QA environment are slow
or expencive to call.

Instant response: Mocking HTTP means that you can receive consistently instantaneous responses.

- Keep working when servers are down: Maybe the existing servers is unreliable. With the mock api you can keep working even if the servers are down.

- Rapid prototyping: Or if you haven't decided how to design your web services,
mocking allows you to rapidly prototype different potential
response shapes and see how they work with your app.

- Avoid inter-team bottlenecks: Perhaps a separate team is creating the service for your app,
by mocking the service calls, you can start coding immediately and switch to hitting real web services when
they're ready, you just need to agree on the API's proposed
design and mock it accordingly, finally, maybe you need to 

- Work Offline: Mocking allows you to continue working while you're offline.

With JSON server you create a fake database using static JSON, then when you start up your JSON server
it creates a web service that works with your static JSON behing the scenes, so when you delete, add or edit records,
it actually updates the file.
So this provides a full simulation of a real working API but against local mock data that's just sitting in a static
file, this is really iseful because the app feels fully responsive and you don't have to go throught the work
of standing up a local database and web server by hand.

JSON schema faker generates fake data for you. You specify the data type you like, such as a string etc and it will generate random data which you can write to a file.


