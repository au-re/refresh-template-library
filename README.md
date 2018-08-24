# Refresh Template - React Component Library

[![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/)

> A component library template built from the [create-react-app](https://github.com/facebook/create-react-app) boilerplate.

View it live [here](https://au-re.github.io/refresh-template-library/).

## Tech Stack

| frontend          |             |
| ------------------|-------------|
| view library      | [react](https://reactjs.org/) |
| styling           | [styled-components ](https://github.com/styled-components/styled-components) |
| boilerplate       | [create-react-app](https://github.com/facebook/create-react-app)|
| documentation     | [storybook](https://github.com/storybooks/storybook) |

## Requirements

You will need the following software installed on your machine:

- [node](https://nodejs.org/en/)

We recomend installing **node** throught [nvm](https://github.com/creationix/nvm), as well as
updating [npm](https://www.npmjs.com/) to version >=5.

## Getting started

You can setup a new project based on this boilerplate using [Yeoman](http://yeoman.io).

First, install Yeoman and generator-refresh using [npm](https://www.npmjs.com/).

```bash
npm install -g yo
npm install -g generator-refresh
```

Then generate your new project:

```bash
yo refresh <my-project>
```

Navigate to the root of the project and install the dependencies:

```sh
cd <my-project>
npm i
```

Once the dependencies are installed, you can launch the documentation and view your components in
isolation:

```sh
npm run start
```

To include a component in the storybook, simply add a `<componentName>.stories.js` file in your
component folder, containing the stories you want to show. Have a look at the `Button` component for
an example.

## Scripts

A set of scripts are provided for you to test, build and analyze the project.

### Test

You can run all tests in the project with the following command:

```sh
npm run test
```

You can also generate a website with information on the code coverage with:

```sh
npm run test -- --coverage
```

This will generate a website in the folder `coverage`. You can launch it with any server of your
choice, for example [serve](https://www.npmjs.com/package/serve).

```sh
npm i -g serve && serve coverage
```

### Build

You can build a production ready version of your library by running:

```sh
npm run build
```

This will create a build folder containing your library.

You can also build a production ready version of you documentation by running:

```sh
npm run build:storybook
```

This will create a folder called `storybook-static` with your documentation.

### Deploy

After building your documentation, you can deploy it as a gh-page.
Make sure to add a homepage value in your `package.json` like so:

```json
{
  "homepage": "https://my-github-name.github.io/my-library/",
}
```

Then simply run:
```sh
npm run deploy
```

### Dependency map

You can generate a map of all dependencies, this can be very usefull when trying to identify a
library causing bloat to the application. After building your application you can generate a map,
by running:

```sh
npm run analyze
```

This will look into your `build` folder and open an interactive map of the dependencies in your
browser.

## License

[MIT](https://github.com/au-re/fresh-start/blob/master/LICENSE)
