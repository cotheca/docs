
# The Cotheca Docs

This repository contains the what and hows of the Cotheca project, like:
- [What exactly is Cotheca](./COTHECA.md)
- [How to contribute to the project](./CONTRIBUTING.md)

And definitely more in the future. Still figuring things out.

## Table of contents
The following table of contents only lists important or relevant files and directories.

  - [**README**.md](./README.md)
    This document. Hopefully points you towards what you are looking for.
  - [**COTHECA**.md](./COTHECA.md)
    What is Cotheca and what it is trying to accomplish.
  - [**CONTRIBUTING**.md](./CONTRIBUTING.md)
    A quick guide on how to contribute to any Cotheca product.
  - [**LICENSE**](./LICENSE)
    Legal stuff that says you can use any of this for whatever purpose as long as you let others know about Cotheca.

  
  - [`contributing/`](./contributing)
    Section about contributing to Cotheca products (i.e. the procedures and practices to contribute code).
    - [**development-cycle**.md](./contributing/development-cycle.md)
     The development cycle used by all Cotheca repositories.

    - [**documentation-practices**.md](./contributing/documentation-practices.md)
      The documentation practices expected for all Cotheca repositories

    - [**forking-and-branching**.md](./contributing/forking-and-branching.md)
      The forking and branching practices used by all Cotheca repositories.

    - [**release-cycle**.md](./contributing/release-cycle.md)
      The release cycle used in all Cotheca repositories for distributing binaries or redistributable packages.

    - [**versioning**.md](./contributing/versioning.md)
    The general versioning convention used by all Cotheca products.


  - [`templates/`](./templates)
    Section for templates to be used as starting points for Cotheca products to standardize development.
    
    - [`.github/`](./templates/.github)
      Contains templates for GitHub features.
    
      The folder name tries to reflect that these are items that you place on the hidden GitHub directory of the repository, like `@cotheca/docs/.github`, where `docs` is the repository name and `.github` is the hidden GitHub directory where pull requests and issue templates are placed so that GitHub can recognize them.
      
      All of the file names in the `./templates/.github` are the actual names of the files as expected by GitHub.

      - [`ISSUE_TEMPLATE/`](./templates/.github/ISSUE_TEMPLATE)
        Contains issue templates that are meant to be placed in the `@user/repo/.github/ISSUE_TEMPLATE` directory, so that GitHub recognizes them.

    - [`gitignore-templates/`](.templates/gitignore-templates)
	 Templates for ignore files for git for different purposes.


## Credits
2023 **The Cotheca Contributors**