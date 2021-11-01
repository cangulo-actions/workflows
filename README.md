# cangulo workflows

## Workflows based on [NUKE](https://nuke.build)
* ### [Calculate Next Release Number](.github/workflows/calculate-next-release-number.yml):
  * Calculate the next release number based on the conventional commits provided in the PR which triggers the workflow
  * Conventional Commits settings should be provided following the gh action: [cangulo.nuke.releasecreator](https://github.com/cangulo-actions/cangulo.nuke.releasecreator)

* ### [Validate Commits](.github/workflows/validate-commits.yml):
  * Validate the commits provided in the PR which triggers the workflow
  * Commits settings should be provided following the gh action: [cangulo.nuke.prcommitsvalidations](https://github.com/cangulo-actions/cangulo.nuke.prcommitsvalidations)


* ### [Release New Version](.github/workflows/release-new-version.yml):
  * Release a new version when a PR is merged into `main`. 
    * updates the version tracker file with the new version number
    * Updated the changelog with the changes merged, those are extracted from the commit messages
    * Tag the `main` branch with the release number
  * Settings should be provided following the gh action: [cangulo.nuke.releasecreator](https://github.com/cangulo-actions/cangulo.nuke.releasecreator)