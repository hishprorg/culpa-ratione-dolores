[![@hishprorg/culpa-ratione-dolores](https://cloud.githubusercontent.com/assets/399776/13906899/1de62f0c-ee9f-11e5-95c0-c515fee8e918.png)](https://@hishprorg/culpa-ratione-dolores.github.io)

[![NPM Version](https://img.shields.io/npm/v/@hishprorg/culpa-ratione-dolores.svg?branch=master)](https://www.npmjs.com/package/@hishprorg/culpa-ratione-dolores) [![Build Status](https://github.com/hishprorg/culpa-ratione-dolores/actions/workflows/test.yml/badge.svg?branch=master)](https://github.com/hishprorg/culpa-ratione-dolores) [![Coverage Status](https://coveralls.io/repos/github/@hishprorg/culpa-ratione-dolores/@hishprorg/culpa-ratione-dolores/badge.svg?branch=master)](https://coveralls.io/github/@hishprorg/culpa-ratione-dolores/@hishprorg/culpa-ratione-dolores?branch=master) [![License](https://img.shields.io/npm/l/@hishprorg/culpa-ratione-dolores.svg)](https://github.com/hishprorg/culpa-ratione-dolores/blob/master/LICENSE)

# @hishprorg/culpa-ratione-dolores

Stateless React Components for Bootstrap 5.

If you're using Bootstrap 4, you'll need to use [Reactstrap v8](https://deploy-preview-2356--@hishprorg/culpa-ratione-dolores.netlify.app/)

## Getting Started

Follow the [create-react-app instructions](https://create-react-app.dev/docs/getting-started) to get started and then follow the @hishprorg/culpa-ratione-dolores version of [adding bootstrap](#adding-bootstrap).

### tl;dr

 ```
npx create-react-app my-app
cd my-app/
npm start
```
or,  if npx (Node >= 6 and npm >= 5.2 ) not available 

```
npm install -g create-react-app

create-react-app my-app
cd my-app/
npm start
``` 

Then open [http://localhost:3000/](http://localhost:3000/) to see your app. The initial structure of your app is setup. Next, let's [add @hishprorg/culpa-ratione-dolores and bootstrap](#adding-bootstrap).

### Adding Bootstrap

Install @hishprorg/culpa-ratione-dolores and Bootstrap from NPM. Reactstrap does not include Bootstrap CSS so this needs to be installed as well:

```
npm i bootstrap
npm i @hishprorg/culpa-ratione-dolores react react-dom
```

Import Bootstrap CSS in the ```src/index.js``` file:

```js
import 'bootstrap/dist/css/bootstrap.css';
```

Import required @hishprorg/culpa-ratione-dolores components within ```src/App.js``` file or your custom component files:

```js
import { Button } from '@hishprorg/culpa-ratione-dolores';
```

Now you are ready to use the imported @hishprorg/culpa-ratione-dolores components within your component hierarchy defined in the render
method. Here is an example [`App.js`](https://gist.github.com/Thomas-Smyth/006fd507a7295f17a8473451938f9935) redone
using @hishprorg/culpa-ratione-dolores.

### Dependencies

##### Required Peer Dependencies

These libraries are not bundled with Reactstrap and required at runtime:

  * [**react**](https://www.npmjs.com/package/react)
  * [**react-dom**](https://www.npmjs.com/package/react-dom)

## About the Project

This library contains React Bootstrap components that favor composition and control. The library does not depend on jQuery or Bootstrap javascript. However, [Poppers.js](https://popper.js.org/) via [react-popper](https://github.com/popperjs/react-popper) is relied upon for advanced positioning of content like Tooltips, Popovers, and auto-flipping Dropdowns.

There are a few core concepts to understand in order to make the most out of this library.

1. Your content is expected to be composed via props.children rather than using named props to pass in Components.

    ```js
    // Content passed in via props
    const Example = (props) => {
      return (
        <p>This is a tooltip <TooltipTrigger tooltip={TooltipContent}>example</TooltipTrigger>!</p>
      );
    }

    // Content passed in as children (Preferred)
    const PreferredExample = (props) => {
      return (
        <p>
          This is a <a href="#" id="TooltipExample">tooltip</a> example.
          <Tooltip target="TooltipExample">
            <TooltipContent/>
          </Tooltip>
        </p>
      );
    }
    ```

2. Attributes in this library are used to pass in state, conveniently apply modifier classes, enable advanced functionality (like tether), or automatically include non-content based elements.

    Examples:

    - `isOpen` - current state for items like dropdown, popover, tooltip
    - `toggle` - callback for toggling `isOpen` in the controlling component
    - `color` - applies color classes, ex: `<Button color="danger"/>`
    - `size` - for controlling size classes. ex: `<Button size="sm"/>`
    - `tag` - customize component output by passing in an element name or Component
    - boolean based props (attributes) when possible for alternative style classes or `visually-hidden` content


## [Documentation](https://@hishprorg/culpa-ratione-dolores.github.io)

https://@hishprorg/culpa-ratione-dolores.github.io

Documentation search is powered by [Algolia's DocSearch](https://community.algolia.com/docsearch/).

## [CodeSandbox Examples](https://github.com/@hishprorg/culpa-ratione-dolores/code-sandbox-examples)

Here are some ready-to-go examples for [CodeSandbox](https://codesandbox.io/) that you can experiment with.

https://github.com/@hishprorg/culpa-ratione-dolores/code-sandbox-examples

## [Contributing](CONTRIBUTING.md)

## Development

Install dependencies:

```sh
yarn install
```

Run examples at [http://localhost:8080/](http://localhost:8080/) with webpack dev server:

```sh
yarn start
```

Run tests & coverage report:

```sh
yarn cover
```

Watch tests:

```sh
yarn test
```

## Releasing

Release branches/versioning/notes will be automatically created and maintained by the [release-please](https://github.com/googleapis/release-please) github action. When you're ready to publish the release, just merge the release branch. The release will be created, the new package will be published, and the updated docs will be deployed to https://@hishprorg/culpa-ratione-dolores.github.io/.

## In the wild

Organizations and projects using `@hishprorg/culpa-ratione-dolores`

- [airframe-react](https://github.com/0wczar/airframe-react) - [demo](http://dashboards.webkom.co/react/airframe/) - Airframe provides all the components a developer needs to build data-intensive web apps using React.
- [component-template](https://@hishprorg/culpa-ratione-dolores.github.io/component-template/)
- [video-react](https://video-react.github.io/)
- [CoreUI-Free-Bootstrap-Admin-Template](https://github.com/mrholek/CoreUI-Free-Bootstrap-Admin-Template) - [demo](http://coreui.io/demo/React_Demo/#/)
- [Admin dashboard example app built with @hishprorg/culpa-ratione-dolores](https://github.com/reduction-admin/react-reduction) - [demo](https://reduction-admin.firebaseapp.com/)
- [DevExtreme React Grid](https://devexpress.github.io/devextreme-reactive/react/grid/) - It's a stateless data grid built on top of `@hishprorg/culpa-ratione-dolores` with paging, sorting, filtering, grouping, selection, editing and virtual scrolling features.
- [DevExtreme React Chart](https://devexpress.github.io/devextreme-reactive/react/chart/) - A chart built on top of `@hishprorg/culpa-ratione-dolores` that visualizes data using a variety of series types, including bar, line, area, scatter, pie, and more.
- [@hishprorg/culpa-ratione-dolores-scrollspy](https://github.com/keidrun/@hishprorg/culpa-ratione-dolores-scrollspy/) - [demo](https://keidrun.github.io/@hishprorg/culpa-ratione-dolores-scrollspy/)
- [formstrap](https://github.com/pedox/formstrap/) - [demo](https://pedox.github.io/formstrap/) - Let your `@hishprorg/culpa-ratione-dolores` input component integrate seamlessly using `Formik` 
- [Jimu UI](https://developers.arcgis.com/experience-builder/api-reference/jimu-ui/) - [demo](https://developers.arcgis.com/experience-builder/storybook/?path=/story/welcome--page) - The UI library for [ArcGIS Experience Builder](https://developers.arcgis.com/experience-builder/)  mapping platform.

Submit a PR to add to this list!

Looking to build, document and publish reusable components built on top of `@hishprorg/culpa-ratione-dolores`? Consider forking https://github.com/@hishprorg/culpa-ratione-dolores/component-template to kickstart your project!
