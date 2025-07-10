# AAGI-AUS GitHub Repositories Guidelines

### Contents

- [Introduction](#introduction)
- [Basic Repository Requirements](#basic-repository-requirements)
- [Licencing](#licencing)
- [GitHub Repository Management Practices](#github-repository-management-practices)
- [Documentation Standards](#documentation-standards)

## Introduction

These guidelines aim to establish best practices and a standard operating procedure for managing GitHub repositories within the AAGI-AUS GitHub page. By following these practices, we ensure that our AAGI project outputs and software tools are of a high quality, and that they uphold the professional standards of the AAGI brand and image. We ensure that our project outputs are reproducible, and that our open-source software is well-documented and available to colleagues, collaborators and end-users.

These guidelines are written to be broad and programming language agnostic, and they incorporate robust software development principles from the [rOpenSci Dev Guide](https://devguide.ropensci.org/) where applicable. Where the AAGI-AUS repository guidelines clash with established practice for specific programming languages or software ecosystems, reasonable judgement should be applied: aim to incorporate the established norms as much as possible, but without negatively impacting the repository consistency or AAGI branding.

See the associated [AAGI-AUS GitHub Repository Setup Checklist](/checklist.md) for a useful checklist that summarises the essential repository setup steps.

## Basic Repository Requirements

Most of the AAGI-AUS repositories will fall into one of the following three categories:

1. _Software repositories_, containing code files for software, libraries, or tools developed through AAGI activities.
1. _Data repositories_, containing datasets with raw or processed data, together with metadata descriptions.
1. _Documentation repositories_, which contain documents for AAGI projects, or presentations, or other similar works.

In all cases, AAGI-AUS repositories are required to have a name, a licence, and a README.

### Repository Name and Description
All repositories on the AAGI-AUS GitHub need an informative name, as well as a brief description describing the purpose of the repository.

If your repository is for a software tool or library that you are developing for some software ecosystem, it is worth Googling the name of your repository to make sure that it is unique within that ecosystem. For instance, if you are writing an R package, try to make sure that the name of your R package does not already exist as some package on CRAN or Bioconductor. You can use the `pkg_name_check` function of the [**pak** package](https://cloud.r-project.org/web/packages/pak/index.html) to help you check that your package name is distinguishable and appropriate.

### Repository Licence (Or Declaration of No Licence)
All AAGI-AUS software, data and documentation repositories should include licencing information that informs end-users about what they may (or may not) do with the code/data.

- If you are licencing software _and the software can be released open-source_, it is recommended to use one of the open-source software licences, such as the MIT Licence or one of the GPL Licences. You can include the licence text verbatim in a LICENSE[^1] (or LICENSE.md) file inside your repository.
- If you are licencing data or documentation _and the data/documentation can be released for public use_, it is recommended that you use one of the Creative Commons licences. Generally, the CC-BY 4.0 is appropriate for most cases.
- If you are _not_ licencing the software/data for any reason (in which case end-users have no licenced rights to use or modify it), you are required to clearly and explicitly declare this in the README.
See the [Licencing](#licencing) section for more information.

[^1]: Note the Americanised spelling for the filename: LICENSE, not LICENCE.

### Repository README
AAGI-AUS GitHub repositories must have a README.md file that provides information for collaborators and end-users. In the README file, typically you want to include:

- **Description:** An overview of the software/data in the repository, including a brief explanation of the AAGI project for which this is an output (where relevant).
- **Install Instructions:** A readable, step-by-step guide for how to install the software/load the data.
- **Usage Examples:** Concise usage examples, showing how to use the software/data (for end-users).
- **Contribution Instructions:** Information regarding how to contribute to the software development or set up a development environment (for collaborators).
- **Dependencies:** Notes about any system or package dependencies that are required to use your software or data (including install instructions or a link to install instructions, as relevant).
- **Licence Information:** Mention the licence for your repository if it has one and include a link to the LICENSE or LICENSE.md file. If your repository is not licenced, you must note this fact unambiguously in the README so that there is no confusion about what end-users can/cannot do with the software or data.
- Any other pertinent information regarding usage, citation, acknowledgements, and so on.

Where possible, include _code snippets_ that viewers can copy-paste for the software installation or usage examples. Use graphics liberally to showcase the software/data or its features. GitHub [repository badges](https://github.com/dwyl/repo-badges) can also be used to show build status, code testing coverage, version information, and other metrics.

### Repository Visibility
All repositories on the AAGI-AUS GitHub page are required to be (eventually) _public_. Note that _private_ repositories can still be created, and these are useful for limiting visibility/access to the repository in early development until you are ready for a proper public release. However, if you never intend for the code or data in your repository to be made available to the public, then the AAGI-AUS GitHub repository is not the appropriate place to host it.

### Other Recommended Repository Requirements
You should consider whether you need one of the following recommended files in your repository:

- A CONTRIBUTING file, which outlines how others can contribute to the project. For projects that have special requirements for contribution, having these requirements in a separate file can help prevent the README from becoming too verbose.
- A CODE_OF_CONDUCT.md file, which explains the expected standards of behaviour for repository contributors. If you decide to include a Code of Conduct, we recommend adopting the [Contributor Covenant](https://www.contributor-covenant.org/), which is widely used across open-source software projects and establishes clear standards for respectful collaboration.
- A SECURITY.md file, which can be used to explain your repository’s security policy and the procedures for reporting vulnerabilities. In GitHub this file is particularly useful for integrating with GitHub Security Advisories to automate the disclosure and publishing of the vulnerabilities to collaborators and users that may be affected. See the [GitHub Security Policy documentation](https://docs.github.com/en/code-security/getting-started/adding-a-security-policy-to-your-repository) for more information on how to set up and work with a SECURITY.md file if you believe your repository may benefit from having one.

Additionally, consider setting up and requiring authenticated commits, to help ensure traceability and accountability. Check the [GitHub Commit Signature Verification documentation](https://docs.github.com/en/authentication/managing-commit-signature-verification/about-commit-signature-verification) for more information.

## Licencing

Choosing an appropriate licence for your AAGI-AUS repository is essential to clarify the conditions under which collaborators and end-users can use, modify, and distribute your work. If your repository can be licenced, it should include a LICENSE (or LICENSE.md) file in the root directory that contains the terms of the licence under which users may use the software (or data/documentation). If your repository is not licenced, then you must communicate this to prospective users and collaborators in the README.

Note that for almost all AAGI projects, the GRDC and other co-owning parties must be consulted before any code, data or documentation is licenced and/or disseminated to the public. Your GRDC Manager for the respective investment must be a part of the licencing discussions, and you are advised to leave your repository with no licence until this discussion has taken place among all interested parties.

For data in an AAGI-AUS repository that is licenced under a Creative Commons licence, in some cases you will require that this data also have its metadata uploaded to the [GRDC Data Catalogue](https://data.grdc.com.au/home/). In such a case, there will be a corresponding line for the dataset recorded in the IPPO Register for the investment.

### Recommended Licences
More general details about the differences between open-source licences can be found at the website https://choosealicense.com/. For AAGI-AUS repositories, we typically recommend the following licences based on the nature of the repository’s contents.

**Licences for Software Repositories:**

- [**MIT Licence:**](https://choosealicense.com/licenses/mit/) The MIT licence is simple and permissive, allowing others to use your code and software for any purpose while only requiring that licence and copyright notices be preserved. Many of the current AAGI-AUS software repositories use this licence.
- [**GNU General Public Licence (GPL) v3:**](https://choosealicense.com/licenses/gpl-3.0/) The GNU GPLv3 is a strong "copyleft" licence that requires distribution of the source code upon request and ensures that all derivative works will remain open-source with the same licence terms.

**Licences for Data Repositories:**

- [**CC-BY 4.0:**](https://choosealicense.com/licenses/cc-by-4.0/) The Creative Commons Attribution 4.0 International licence permits almost any use of the data, subject to providing credit to the data authors and keeping all licence and copyright notices intact. The CC-BY 4.0 is appropriate for most cases where your data is licenced to be publicly available.
- [**CC-BY-SA 4.0:**](https://choosealicense.com/licenses/cc-by-sa-4.0/) The Creative Commons 'Share-Alike' licence, a modification of the CC-BY 4.0 that includes requirements that data derivatives are also licenced under the CC-BY-SA 4.0.

**Licences for Documentation Repositories:**

- [**CC-BY 4.0:**](https://choosealicense.com/licenses/cc-by-4.0/) The Creative Commons Attribution 4.0 International licence is almost always appropriate for documentation, educational resources and other media that you wish to be usable or modifiable by the public.

_**Licences that are not recommended:** 'Public domain' licences, such as the Unlicense and the Creative Commons Zero (CC0), are never appropriate for AAGI software and research outputs. AAGI projects are funded by the GRDC and contributed to by research partners, government departments, and other collaborators, all of which have interests and moral rights to attribution for their work or data (and they usually have commercial interests in AAGI project outputs too). A public domain licence denies these interests._

### Licence Compatibility Considerations

Be aware of any dependencies in your software project that may constrain your choice of licence. When you incorporate third-party code or bundle third-party libraries with your software, you are bound by the terms of the licence for those components. If you incorporate code that is licenced under the GNU GPLv3, your software must in turn be licenced fully under the GNU GPLv3, and this may be an issue that precludes the inclusion of those components in your software project in extreme cases.

## GitHub Repository Management Practices

Effective repository management practices are crucial for the development of AAGI’s software and other project outputs, and the AAGI-AUS GitHub provides excellent tools for this management. Use GitHub features such as repository branching, version control, issue trackers and pull requests to help you organise your collaborations and coordinate the development work.

### Repository Branching
Use branches to help you keep track of the different development streams that may exist in your repository and ensure that different collaborators are not accidentally overwriting one another’s work. Label each branch with an informative name, The [GitFlow branching model](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) provides a useful naming convention for branches that is recommended for use in AAGI-AUS repositories. Consider using some (or all) of the following branches for your repository management:

- **main** (or **master**): The default branch for any new repository. For a larger project with multiple contributors, it is recommended that you keep _main_ for your stable, tested and confirmed-working version of your code or data/documents.
- **develop** (or **dev**): You can use a separate _dev_ branch for the active code development. Insulating the development like this is a great way to ensure that your main repository is always production-ready for end-users to download, and that any (potentially code-breaking) changes are kept isolated to the _dev_ branch so that they can be found and fixed without impacting end-users.
- **feature/<name>**: When your repository has multiple contributors developing separate features, you can have each contributor split the _dev_ branch into a separate _feature/..._ branch. Use a descriptive name for the feature. For example, if your branch is adding a new function called `generate_design()` to a package, you could call the branch _feature/generate-design_ or something similar.
- **bugfix/<name>**: Similarly, if you have bug fixes or code updates that you want to work on separately from the main _dev_ branch, you can split these out into _bugfix/..._ branches using a descriptive name for the bug. For example, you may have a branch called _bugfix/resplot-buffer-error_ to develop and test a fix for a bug due to some buffer issue in a function called `resplot()`.

Branch merges should work their way back up the development tree in a methodical way. Typically, you would merge _feature/..._ and _bugfix/..._ branches back into the _dev_ branch once they were confirmed to be working, and then you would merge the _dev_ branch back into _main_ once you had thoroughly tested and were set to make a proper production-ready update to your software or data repository.

It is advisable to set up _branch protection rules_, to help ensure that your critical _main_ branch is protected from changes that could break workflows for end-users and repository collaborators. See the [GitHub Docs guide on managing branch protection rules](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/managing-a-branch-protection-rule) for more information on how to set these rules.

### Version Control

GitHub keeps track of changes made in a repository using _commits_, which are descriptive snapshots of the repository branch at different points during the development. The history of these commits is retained in a log that allows for easy auditing and tracking of code changes.

For the AAGI-AUS repository, it is highly recommended to use descriptive commit messages. At a minimum, describe the "what" behind your code update. To make the best commit messages, try to describe the "why" behind the update as well. The following are examples of excellent commit messages:[^2]

- "adds header and footer to full-length report docx template"
- "address #2 – modified abyss with ng50"
- "Closing curl connections manually rather than relying on the GC to be quick enough"

The following are okay commit messages (but they could be better):

- "corrected labels"
- "Updated some documentation"
- "Fixed typo"

The following are examples of unhelpful commit messages. Try to avoid these:

- "Update README.md"
- "minor change"
- "Save my work"

Try to make your commits small, frequent, and focused on a single issue or feature. This helps to create a detailed repository history and makes it easy to determine where to rollback code changes if something breaks later.

[^2]: All examples were taken from active repositories on the AAGI-AUS GitHub, circa June 2025.

### Be Careful What You Commit!
As GitHub is set up to keep a detailed history of changes, this means that it is also quite difficult to completely remove any traces of files or changes that you did not intend to make. Do not make any commits that contain:

- Superfluous or auto-generated output files. Add these to the repository’s _.gitignore_ instead so that you do not accidentally upload them with an errant `git add *`, which is typically how these local files end up pushed to your GitHub repository.
- Large binary files. GitHub starts emailing you warnings if you have uploaded files of sizes 50MB or larger, or if your repository hits 5GB total, and you can risk having your repository removed. Generally, files this large do not belong in a GitHub repository anyway, and you should be using alternative storage solutions.
- Sensitive information such as classified data files, Personally Identifiable Information (PII), or authentication credentials and API keys.

If you have accidentally made a commit that contains sensitive information, alert an AAGI senior software developer immediately. It is _not enough_ to simply remove the file and push a new commit—the entire repository history needs to be rewritten (and depending on the severity of the disclosure of sensitive information, GitHub Support may need to be contacted to help remove the sensitive material). See this [GitHub Docs guide](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository) for more information.

### Semantic Versioning for Releases

For packages and other more formal software development projects, it is recommended to use _semantic versioning_ to label your package with meaningful version numbers based on its development. The most useful convention is MAJOR.MINOR.PATCH. 

As an illustrative example, if your package was called _mypkg_, then _mypkg v1.1.2_ would be the version of the package with major version 1, minor version 1, and patch version 2. You would apply your development updates in a disciplined way as follows:

- You would update the MAJOR version number (and reset the MINOR and PATCH numbers) for any significant update to the software package: in this case, your new version of the package would be _mypkg v2.0.0_. You update the MAJOR version number for any change that introduces an important new feature, removes an old feature, or otherwise could be anticipated to break the workflow of your end-users.
- You would update the MINOR version number (and reset the PATCH number) for any smaller feature update to the software: in this case, your new version would be _mypkg v1.2.0_. Update the MINOR version number for small changes that add new functionality, but are otherwise not anticipated to cause any significant differences in the way that end-users would expect to use your package.
- You would update the PATCH version number for any bug fixes or other tiny changes: in this case, your new package version would be _mypkg v1.1.3_. Update the PATCH version number only when you make bug fixes or minuscule changes (i.e., changes that do not affect the package features or functionality), which should have no effect on how your end-users expect to use your package.

To mint a new version of your package, you would commit using git tags for the releases (making sure to transfer the tags to the remote GitHub repository by specifying `origin --tags` in the push command):

```bash
git tag -a v1.1.3 -m "Version 1.1.3"
git push origin --tags
```

You may wish to use separate repository branches for different versions to help keep your code organised: for instance, you could have a branch called _release/v1.2.0_ that isolates the development and testing work ahead of an 'official' version 1.2.0 release of your software package.

### Issue Tracking

You (and your repository’s end-users) should use GitHub’s _issue tracker_ to keep track of bugs, tasks and feature requests for your software or data. If you are creating an issue, ensure that you:

- Provide a clear and concise title.
- Use the description to explain as much detail as possible about the issue or request. If your issue is a suspected bug, include relevant details about the environment in which you encountered that bug (e.g., operating system, R/Python versions, versions of other packages that you suspect may be involved, and so on).
- Use labels to categorise your issue. (Is it a bug? A requested feature/enhancement? A question?)

If you are responding/triaging an issue, make sure that you:

- Assign issues directly to repository collaborators, as appropriate, for visible accountability.
- Use @mentions to notify repository collaborators as relevant.
- Inquire about further details from the issue raiser as needed.

Keep in mind that the issue tracker is publicly visible and will often be a direct interface to the wider community. Your conduct when creating or responding to issues also reflects upon AAGI’s professional image, as well as that of the Strategic Partners. Aim to respond promptly to questions and issues raised by your end-users. Keep your discussions professional, focused, and relevant to the issue. If an issue is not relevant or cannot be resolved, close the issue—but always include a comment explaining why the issue has been closed.

### Pull Requests

If you (or a collaborator, including external collaborators for open-source repositories) have a separate branch (or fork) that you want merged back into the main branch, you should do this by making a _Pull Request_ (PR) to be reviewed by the repository collaborators. When creating your PR, ensure that:

- You nominate at least one of the repository’s primary contributors to perform a _code review_ of your PR, so that they can check your update for code correctness, adherence to style and documentation guidelines, and functionality. GitHub’s code review features also enable the reviewers to comment on specific code lines and discuss any changes that need to be made before the PR can be merged.
- You include enough information in the description included with the PR to ensure that the reviewers can understand the changes that have been made. Reference issues by number in the issue tracker where relevant (e.g., “Fixes #6”).
- You have checked that your proposed changes pass all of the automated tests, and that any conflicts between the branches have been resolved before merging. Merge conflicts can be best avoided by ensuring that your PRs make only small, focused changes at a time, and that you regularly pull from the target branch to ensure that you stay up-to-date with changes others have made.

To keep your repository organised, it is recommended that the PR branches are removed following a successful merge.

## Documentation Standards

While the exact requirements for documentation will differ depending on the repository (and programming language), strive to aim for a quality of documentation that upholds the professional standards of the AAGI brand. Generally, ensure that your code/software is adequately commented, and that any data has an appropriate level of metadata description to enable end-users to know where it came from and how to use it.

### Software Documentation
Use a consistent commenting and documentation style appropriate to your programming language. In general, try to aim for a level of documentation that would enable a future collaborator, other members of the development team, or even yourself months or years later, to be able to understand what the software is doing, and pick up where you left off. Some recommendations for good documentation practice are listed below for different cases.

#### Scripts

Small scripts (e.g., single file R or Python scripts) do not usually need as much documentation as the other cases. At a minimum, ensure that you include a comment block at the top of the script that contains a brief purpose of the script and who the code author was. Try to limit the length of your code comments to 70-80 characters per line, as these are easier to read in typical code editors. An example might look like:

```r
# This script loads the oats data from project UOA1234-567ABC and
# performs an exploratory analysis of the yield and grain content
# using ASReml.
# Code author: Russell Edson, AAGI-AU
# Date: 25/06/2025
```

Keep in mind that most users running your script will be running it line-by-line in an interpreter, so this means that the extra effort that you put into commenting your code and making the code neat and organised will be noticed and very appreciated. _Include comments liberally_ throughout the script to describe what different parts of the code are doing, especially if the code is doing something complex or using uncommon programming features. Use comments to also highlight and describe any issues that you or an end-user may encounter when running the script.

#### Libraries and Packages

In this case, you want to put more effort into the software documentation than for a script. Ensure that the documentation is in an appropriately machine-readable format, and that you have documented all functions, classes, modules and embedded datasets. This documentation should include:

- The purpose of the class/function/module/dataset.
- Parameter types and descriptions, as relevant.
- Return values and output descriptions, as relevant.
- Illustrative usage examples.

For libraries and packages, be aware that most of your end-users are _not_ going to be looking at the code files when they want to figure out what your software does. Instead, they will be searching through separate documentation files, and usually indirectly by browsing in a help window, using code auto-completion, and other context-aware actions in their programming environment. Most programming languages have facilities that allow you to generate this documentation automatically, provided that you are writing your comments according to a specific style. For example:

- [**roxygen2**](https://roxygen2.r-lib.org/) allows you to generate documentation from your R code files in an automated way, using specific tags to describe the purposes, parameters and return types of your functions, objects and data. Package documentation by Roxygen2 is well-integrated into the R ecosystem, and users of your package will be able to browse the help files/vignettes and get auto-completion and tooltip help when using functions.
- Python code is typically documented using [docstrings](https://realpython.com/documenting-python-code/#docstrings-background), which integrate well with the Python interpreter and various Integrated Development Environments. Docstrings with special formatting and tags are used with tools like [**Sphinx**](https://www.sphinx-doc.org/en/master/) to automatically generate external documentation.
- Other programming languages have similar documentation generators, most of them based on the popular and industry-standard [**Doxygen**](https://www.doxygen.nl/) tooling.

For software libraries and packages, you will typically want to include some _testing_. Most programming languages also provide code testing suites that allow you to set up test cases to check that your functions are working correctly. These test cases are an eminently useful and understated form of documentation for your software, as they help to capture the exact and intended behaviour of your library or application. Further, when you or others make changes to your code, you can then re-run the test cases and make sure that nothing has been broken due to the code changes.

Examples of testing frameworks include:

- For R code, the [**testthat**](https://testthat.r-lib.org/) package is the most popular testing framework and provides user-friendly functionality for writing unit tests for your functions. The test suite is integrated well into the R ecosystem. For Shiny apps, you can additionally use the snapshot-based [**shinytest**](https://rstudio.github.io/shinytest/articles/shinytest.html) package to automate Shiny App button clicks and other interactions.
- Python has a built-in testing framework in the standard library called [**unittest**](https://docs.python.org/3/library/unittest.html), which allows you to write unit tests for your functions and classes. The test framework includes useful features such as the ability to set up test fixtures at the function, class or module level, to streamline testing of larger software libraries and applications.
- Other programming languages will almost certainly include some unit testing framework that you can use, and they all work in similar ways.

Additionally, consider implementing continuous integration and other deployment workflows via GitHub Actions. You can use GitHub Actions to, among other things:

- Automate the running of your tests and deployment checks whenever you or a collaborator pushes a code update to a repository.
- Set up and automatically deploy documentation websites for your software packages or library (e.g., via [GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site), which can be automated via packages like [**pkgdown**](https://pkgdown.r-lib.org/) for R packages or [**ghp-import**](https://pypi.org/project/ghp-import/) for Python projects).

See the [GitHub Actions Quickstart guide](https://docs.github.com/en/actions/writing-workflows/quickstart) for more details on how to set these up.

#### Large Packages and Software Applications

Larger software development efforts will need significant effort put into their documentation. All of the recommendations for the **Libraries and Packages** case apply here too, but they now apply as _minimum requirements_ rather than best-practice recommendations:

- You are _required_ to ensure that you are documenting all functions, classes, modules and datasets in a manner that facilitates the automated generation of Doxygen-style documentation.
- You are _required_ to have a testing framework in place, with a large volume of unit tests to document and assert the correct behaviour of your library or software application.
- You are _required_ to have a continuous integration workflow, to automate deployments and prevent code updates from breaking your software.

For large software applications with many components, consider also including architectural documentation, which can be helpful for onboarding collaborators as well as formally specifying (and limiting) the scope of the software development. [Software requirements specifications](https://www.computer.org/resources/software-requirements-specifications) and charts such as [UML diagrams](https://drawio-app.com/blog/uml-class-diagrams-in-draw-io/) are useful for capturing the top-level view for your software, including each of the different components and how they must couple and communicate with each other. These can be included in your GitHub repository.

### Data Documentation

Make sure that you provide _metadata_ about your datasets if you are storing them in an AAGI-AUS GitHub repository. A good way of doing this is to have a plaintext file containing the dataset metadata description and include this file together with the dataset in your repository. However, at a minimum, ensure that you have a reasonably detailed description of the data somewhere, such as in the GitHub repository README.

The [Cornell University Metadata Template](https://cornell.app.box.com/v/ReadmeTemplate) is a popular and useful plaintext template for dataset documentation, which includes specific metadata fields that you should fill in to give your end-users the best chance of understanding and using your data for their own purposes. Regardless of how you decide to document your data, to generate high-quality metadata records, consider answers to the following questions that your end-users might have _about_ your dataset:

1. Who collected the data?
1. When was the data collected/generated?
1. Where was the data collected? (If relevant.)
1. Why was the data collected? (I.e., what was the purpose of the experiment that the data are from?)
1. How was the data collected or generated? (E.g., sampling methodology, data processing, etc.)

And how your end-users can _use_ your dataset:

6. What are the names of the variables contained in the dataset?
1. How were these variables measured? (I.e., what are their units?)
1. What are the data types for these variables? (In particular, how are N/A or missing values represented?)
1. Are there any restrictions (licencing, access conditions, copyrights) that apply to the data?
1. How does someone load the data? (I.e., are any special or proprietary programs needed?)

And the extra contextual information that your end-users would need to fully _understand_ your dataset:

11. Are there any abbreviations or uncommon notations used in the data which need explaining?
1. Are any data values missing or in doubt, and if so, why?
1. Were there any adverse conditions that affected the collection or generation of the data?

Your aim with the metadata should be to produce an enduring record that helps to answer such questions.

#### Archiving on Zenodo and Uploading Metadata to the GRDC Data Catalogue

It is highly recommended that you archive any open data/metadata repositories that you upload to the AAGI-AUS GitHub to [Zenodo](https://zenodo.org/). This has three main benefits:

1. GitHub is a proprietary third-party hosting service that (while unlikely) could be shut down or restrict access suddenly. [Zenodo, on the other hand,](https://about.zenodo.org/policies/) is backed by CERN, with guarantees that its data hosting will be supported for at least the next 20 years, and succession plans in place to handle repository transfer in the event of closure.
1. Repositories and other data uploaded to Zenodo is minted with a [Digital Object Identifier](https://www.doi.org/) (DOI), which is a persistent and unique identifier that you can use to reference and link to your repository/data in journal articles, reports, and other formal documents.
1. Zenodo is well-integrated with GitHub. When you make a new release on GitHub after linking, Zenodo will automatically archive that new release for you. This includes minting a new release-specific DOI, so that you can point to specific releases of your dataset, in addition to the general DOI which always points to the latest version.

Note that depending upon the project for which you are producing AAGI outputs, you may have discussed with your GRDC Manager to upload the dataset metadata to the [GRDC Data Catalogue](https://data.grdc.com.au/home/). In this case, you can follow the GRDC’s guide (accessible via [this link](https://grdc.com.au/__data/assets/pdf_file/0024/603177/GRDC-Guideline-for-data-upload-and-metadata-creation-in-Zenodo-for-Research-Partners-v1.1.pdf), with instructional videos created by the Centre for Crop and Disease Management available [here](https://www.ccdm.com.au/dataharvestresources/grdc-guideline-for-data-upload-and-metadata-creation-in-zenodo-part-1/)) for populating and uploading metadata records to the _GRDC Zenodo Community_. Data records in the GRDC Zenodo Community are automatically harvested to the Data Catalogue on a regular basis.
