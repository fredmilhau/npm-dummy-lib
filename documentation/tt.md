
## npm scoped packeges

@fredmilhau/npm-dummy-lib

https://nitayneeman.com/posts/understanding-scoped-packages-in-npm/

By default, scoped packages are published with private visibility. To publish a scoped package with public visibility, use:

    npm publish --access public.


## npm registry

There are two options for choosing a registry:

    The official public.
    A private one.

To assign the scope with a private registry, use:

npm config set @sample-scope:registry http://sample-registry.com


## structure

create a lib folder and a index.ts file inside of it.

mkdir lib && touch lib/index.ts


## .npmignore

https://docs.npmjs.com/misc/developers#keeping-files-out-of-your-package

By default, the following paths and files are ignored, so there’s no need to add them to .npmignore explicitly:

    .*.swp
    ._*
    .DS_Store
    .git
    .hg
    .npmrc
    .lock-wscript
    .svn
    .wafpickle-*
    config.gypi
    CVS
    npm-debug.log

    Additionally, everything in node_modules is ignored, except for bundled dependencies. npm automatically handles this for you, so don’t bother adding node_modules to .npmignore.

The following paths and files are never ignored, so adding them to .npmignore is pointless:

    package.json
    README (and its variants)
    CHANGELOG (and its variants)
    LICENSE / LICENCE

If, given the structure of your project, you find .npmignore to be a maintenance headache, you might instead try populating the files property of package.json, which is an array of file or directory names that should be included in your package. Sometimes a whitelist is easier to manage than a blacklist.
