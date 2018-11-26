# Nodenv Ansible Role

For installing [Nodenv](https://github.com/nodenv/nodenv) and multiple [NodeJS](https://nodejs.org/en/) versions via Ansible.

Also installs:

- [Node Build](https://github.com/nodenv/node-build)
- [Nodenv Update](https://github.com/nodenv/nodenv-update)
- [Nodenv Rehash](https://github.com/nodenv/nodenv-package-rehash)

Can also globally install [NPM](https://www.npmjs.com/) packages for each installed NodeJS version.

(barely) tested on Ubuntu 14.04 (trusty) and above (currently to 18.04 bionic).

## Variables

Defaults found in `default/main.yml`:

### NodeJS versions

```
node_versions:
  - "7.6.0"
  - "8.13.0"
```

An array list of all nodeJS versions to be installed.

### Default NodeJS version

```
node_default: "7.6.0"
```

The default version of nodeJS to be used if no local version set in `.node-version`.

### Global NPM packages

```
npm_defaults:
  - "grunt-cli"
  - "gulp-cli"
  - "bower"
```

An array list of all NPM modules to be installed globally.  Modules are installed for **all** nodeJS versions.

## License
MIT

## Author Information
This role was created in 2017 by [Richard Chapman](https://chapmanio.uk).
