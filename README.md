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

[Install JHipster](https://jhipster.github.io/installation.html), **the Yarn way!!** I.e. node, yarn, yo, jhipster.

**Attention!** 
In the above link you will be instructed to install the latest version of jhipster with the command `yarn global add generator-jhipster`. There are some problems with the latest versions, so we must install specific version 4.14.5 by typing instead:

```
yarn global add generator-jhipster@4.14.5
```


## Install Gulp (globally)

```
yarn global add gulp
```

We don't actually use it. But without it, we get an ugly error each time we run this tool.

## Install this module

```bash
yarn global add https://github.com/flower-platform/generator-jhipster-entity-replacer
```

If you want a specific branch, then:

```bash
yarn global add https://github.com/flower-platform/generator-jhipster-entity-replacer#my-branch
```

**Note:**
When installing the generator as global, the directory where it will be found is ``c:\Users\<USER>\AppData\Local\Yarn\config\global\node_modules``. Git should be installed on your system. It's probably the case already. If not, you should install it w/ their installer.

And that's it! For apps based on Foundation Platform, there are preconfigured launch configs, so normally you don't need to do the steps below (i.e. "Usage" section). 

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

# Troubleshooting

1) It is possible that **yarn global add <git_repo>** reveals an error which indicates that it is unable to access the git repo.
This was solved by updating to the latest github version.

![alt text](https://user-images.githubusercontent.com/8615775/50286069-e237e500-0466-11e9-9bd2-fe0883d9537b.png)





[npm-image]: https://img.shields.io/npm/v/generator-jhipster-entity-replacer.svg
[npm-url]: https://npmjs.org/package/generator-jhipster-entity-replacer
[travis-image]: https://travis-ci.org/entity/generator-jhipster-entity-replacer.svg?branch=master
[travis-url]: https://travis-ci.org/entity/generator-jhipster-entity-replacer
[daviddm-image]: https://david-dm.org/entity/generator-jhipster-entity-replacer.svg?theme=shields.io
[daviddm-url]: https://david-dm.org/entity/generator-jhipster-entity-replacer
