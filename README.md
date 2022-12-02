# doc-example

An example of how to run a local preview of [Antora](https://docs.antora.org/antora/latest/) documentation

## Context

When building complex documentation using [Antora](https://docs.antora.org/antora/latest/) it's common for a documentation site to be composed from [multiple source repositories](https://docs.antora.org/antora/latest/content-source-repositories/).

When a developer is working on the whole documentation site they would normally run inside a repository crafted for that site which pulls in all of the source repositories.

However when one is working on a specific code repository it can be frustrating to not be able to preview your documentation locally.

This repository gives a simple example of how to add the necessary Antora preview tooling to any code repository.

## Repository layout

|Path or file|Commentary|
|------|------|
|`package.json`|Package configuration, includes necessary documentation dependencies as dev-dependencies|
|`local-antora-playbook.yml`|Antora playbook for running in [author mode](https://docs.antora.org/antora/latest/playbook/author-mode/) |
|`gulpfile.js`|[gulp-js](https://gulpjs.com/) configuration to run the local documentation preview|
|`/docs/tech/`|Example technical documentation, potentially being built into a website external to this repo|
|`/docs/user/`|Example user documentation, potentially being built into a website external to this repo|
|`/docs/local/`|Local-only documentation used in our [author mode](https://docs.antora.org/antora/latest/playbook/author-mode/) oreviuew|

## Running the example

1. clone this repository
2. in your local working directory:
   - `npm install`
   - `npx gulp`
3. visit [http://localhost:5000](http://localhost:5000)
4. make changes to the documentation files and observe the results 
