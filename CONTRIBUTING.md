# Contribution guidelines

You are most welcome to suggest improvements, report
[issues](https://github.com/symfony-si/magento2-sl-si/issues), or send pull
requests:

* Fork this repository over GitHub
* Set up your local repository

  ```bash
$ git clone git@github.com:your_username/magento2-sl-si
$ cd magento2-sl-si
$ git remote add upstream git://github.com/symfony-si/magento2-sl-si
$ git config branch.master.remote upstream
```
* Make changes and send pull request

  ```bash
$ git add .
$ git commit -m "Update files"
$ git push origin
```

## Translation rules

Translations must follow Slovenian translation rules from
[Lugos](https://wiki.lugos.si/slovenjenje:pravila).

## Development practices

Developing the language module and the main Magento store separately requires
a different workflow. After cloning the repository locally, you can just do the
following in package folder:

```bash
# Make sure you have Magento repositories defined in your Composer configuration
composer config repositories.magento composer https://repo.magento.com --global
# Install dependencies for development
composer install
```

## Release process

*(For repository maintainers)*

This repository follows [semantic versioning](http://semver.org). When source
code changes or new features are implemented, a new version (e.g. 1.x.y) is
released by the following release process:

* **1. Update changelog:**

  Create an entry in [CHANGELOG.md](CHANGELOG.md) describing all the changes
  from previous release.

* **2. Tag a new release:**

  Tag a new release version on GitHub.

* **3. Attach a ZIP archive of the language package to a GitHub release**

  Attach ZIP sl_si-1.x.y.zip as a binary file for manual installation and for
  Magento Marketplace.
