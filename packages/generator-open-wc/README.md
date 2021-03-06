# Generator Open WC

[//]: # (AUTO INSERT HEADER PREPUBLISH)

## Usage

This generator is based on [yeoman](http://yeoman.io/). Simply use it like this:
```bash
# in a new or existing folder:
npm init yo open-wc
# requires npm 6 or higher
```

For running specific generators you can do as demonstrated:

```bash
npm i -g yeoman
npm i -g generator-open-wc

yo open-wc:{generator-name}
```

or

```bash
npx -p yo -p generator-open-wc -c 'yo open-wc:{generator-name}'
```


## Scaffold generators

These generators help you kickstart a web component.
You can use these in an empty folder to set up everything you need to get started immediately.

Example usage:
```bash
mkdir foo-bar
cd foo-bar
yo open-wc:scaffold-vanilla
# this will scaffold a new web component + run all available scaffold generators
```


### Available application generators:

- `yo open-wc:starter-app`<br/> 
  This generator scaffolds a new starter application. We recommend using this generator at the start of your web component project. 
  <details>
    <summary>More info</summary>
    <br/>
    This generator will internally run:

      - open-wc:bundling-webpack
      - open-wc:testing
      - open-wc:linting
      - A frontend setup
  </details>
  <br/>

### Available scaffold generators:

- `yo open-wc:scaffold-vanilla`<br/> 
  This generator scaffolds a new web component project for you with all of our recommendations. We recommend using this generator at the start of your web component project. 
  <details>
    <summary>More info</summary>
    <br/>
    This generator will internally run:

      - open-wc:linting
      - open-wc:scaffold-testing
      - open-wc:scaffold-demoing
      - open-wc:automating
  </details>
  <br/>

- `yo open-wc:scaffold-building`<br/> 
  This generator scaffolds a webpack configuration for you with examples to your existing project. 
  <details>
    <summary>More info</summary>
    <br/>
    This generator will internally run:

      - open-wc:building-webpack
      - Plus an index.html and index.js using the [@open-wc/polyfills-loader](https://www.npmjs.com/package/@open-wc/polyfills-loader)
  </details>
  <br/>

- `yo open-wc:scaffold-demoing`<br/> 
  This generator scaffolds a Storybook setup for you with examples to your existing project. 
  <details>
    <summary>More info</summary>
    <br/>
    This generator will internally run:

      - open-wc:demoing
      - Plus Storybook examples
  </details>
  <br/>

- `yo open-wc:scaffold-testing`<br/>
  This generator scaffolds a Karma setup for you with examples to your existing project. 
  <details>
    <summary>More info</summary>
    <br/>
    This generator will internally run:

      - open-wc:testing
      - Plus example tests
  </details>
  <br/>


## Upgrade generators
These generators help you to align your current project with the `open-wc` recommendations.
You can use these to add to an existing project that already contains code for your web component.

Example usage:
```bash
cd existing-web-component
yo open-wc:upgrade
# this will execute all available upgrade generators
```

### Available upgrade generators

- `yo open-wc:linting`<br> 
This generator adds a complete linting setup with ESLint, Prettier, Husky and commitlint to your existing project. 
  <details>
    <summary>More info</summary>
    <br/>
    This generator will internally run:

      - open-wc:linting-eslint
      - open-wc:linting-prettier
      - open-wc:linting-commitlint
  </details>
  <br/>
  

- `yo open-wc:building`<br> 
This generator adds a complete building setup with webpack to your existing project. 
  <details>
    <summary>More info</summary>
    <br/>
    This generator will internally run:

      - open-wc:building-webpack
  </details>
  <br/>


- `yo open-wc:testing`<br>
This generator adds a complete testing setup with Karma, and Karma Browserstack to your existing project. 
  <details>
    <summary>More info</summary>
    <br/>
    This generator will internally run:

      - open-wc:testing-karma
      - open-wc:testing-karma-bs
  </details>
  <br/>
      

- `yo open-wc:demoing`<br>
This generator adds a complete demoing setup with Storybook to your existing project.
  <details>
    <summary>More info</summary>
    <br/>
    This generator will internally run:

      - open-wc:demoing-storybook
  </details>
  <br/>


- `yo open-wc:automating`<br>
This generator adds a complete automating setup with CircleCi to your existing project. 
  <details>
    <summary>More info</summary>
    <br/>
    This generator will internally run:

      - open-wc:automating-circleci
  </details>
  <br/>


### Optional upgrade generators
These generators are not executed with the default upgrade generator.

- `yo open-wc:testing-wallaby`<br>
  This will set up [Wallaby](https://wallabyjs.com/) to enable testing directly in your IDE. For more information, see [testing-wallaby](/testing/testing-wallaby.html).

### Sub generators
These generators are executed with the default upgrade generator.
You can use these generators if you already have an existing project that you would like to add to.

- `yo open-wc:building-webpack`<br>
  This generator adds a build configuration with Webpack to your existing project.

- `yo open-wc:linting-eslint`<br>
  This generator adds linting with ESLint to your existing project.


- `yo open-wc:linting-prettier`<br>
  This generator adds code formatting with Prettier to your existing project.


- `yo open-wc:linting-commitlint`<br>
  This generator adds linting to your git commits with commitlint to your existing project.


- `yo open-wc:testing-karma`<br>
  This generator adds a testing setup with Karma to your existing project.


- `yo open-wc:testing-karma-bs`<br>
  This generator adds a testing setup with Karma and Browserstack to your existing project. This generator requires a manual step of adding your Browserstack credentials to your `.bashrc`. For more information, see [this page](/testing/testing-karma-bs.html#setup).


- `yo open-wc:automating-circleci`<br>
  This generator adds continuous integration with CircleCi to your existing project.

<script>
  export default {
    mounted() {
      const editLink = document.querySelector('.edit-link a');
      if (editLink) {
        const url = editLink.href;
        editLink.href = url.substr(0, url.indexOf('/master/')) + '/master/packages/generator-open-wc/README.md';
      }
    }
  }
</script>
