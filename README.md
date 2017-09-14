# generator-jhipster-entity-replacer
[![NPM version][npm-image]][npm-url] [![Build Status][travis-image]][travis-url] [![Dependency Status][daviddm-image]][daviddm-url]
> JHipster module allowing the customization (via text replace) of the entities generated by importing from JDL.

# Install

## Preparation/cleaning up

**Note:**
JHipster and Yeoman can be installed via Yarn or NPM. From what we have seen there are big subtle issues if both install methods are used. 

* Did you work with JHipster and/or Yeoman via NPM in the past? You can verify by looking in ``c:\Users\<USER>\AppData\Roaming\npm\node_modules\`` for something named ``*jhipster*`` or ``*yo*``.
* If YES, then the safest thing to do is to delete the NPM repo: 
  * ``c:\Users\<USER>\AppData\Roaming\npm\``
  * ``c:\Users\<USER>\AppData\Roaming\npm-cache\``
  
By doing this, other existing node packages are gone as well. But that's no problem; when you'll need them, you can reinstall them using npm. 

## Install JHipster

[Install JHipster](https://jhipster.github.io/installation.html), the Yarn way. I.e. node, yarn, yo, jhipster.

## Install this module:

```bash
yarn global add https://github.com/flower-platform/generator-jhipster-entity-replacer
```
**Note:**
When installing the generator as global, the directory where it will be found is ``c:\Users\<USER>\AppData\Local\Yarn\config\global\node_modules``

# Update

```bash
yarn global upgrade generator-jhipster-entity-replacer
```

# Usage
```bash
cd <project folder (where .jdl file is)>
```
## First time use
```bash
yo jhipster-entity-replacer
```
This will install a hook in ``<project folder (where .jdl file is)>/jhipster/modules/jhi-hooks.json``, and you will be able to use it with the next method.

## Normal use
```bash
yo jhipster:import-jdl <jdl_file> --force
```
### Notes:

- ``--force`` is an optional parameter that indicates to the importer that all the entities must be re-imported regardless they were updated or not in their .jdl. It's recommended, as you won't be bothered by prompts.

[npm-image]: https://img.shields.io/npm/v/generator-jhipster-entity-replacer.svg
[npm-url]: https://npmjs.org/package/generator-jhipster-entity-replacer
[travis-image]: https://travis-ci.org/entity/generator-jhipster-entity-replacer.svg?branch=master
[travis-url]: https://travis-ci.org/entity/generator-jhipster-entity-replacer
[daviddm-image]: https://david-dm.org/entity/generator-jhipster-entity-replacer.svg?theme=shields.io
[daviddm-url]: https://david-dm.org/entity/generator-jhipster-entity-replacer
