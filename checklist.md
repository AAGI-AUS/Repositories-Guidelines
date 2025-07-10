# AAGI-AUS GitHub Repository Compliance Checklist
 
The following checklist is a useful guide to help you manage your AAGI-AUS GitHub repository. The [first section](#1-initial-repository-setup) contains repository preparation instructions, and the [second section](#2-ongoing-repository-compliance) provides some useful review items that you should regularly check to ensure that you are remaining compliant with AAGI-AUS repository standards.

## 1. Initial Repository Setup

### Initialise Your Repository

- [ ] Choose a unique and appropriate name. (You can use Google or `pak::pkg_name_check()` to help.)
- [ ] Include a brief description for the repository.
- [ ] Set your repository’s visibility. Choose _public_, unless you need to temporarily limit visibility/access.
- [ ] Add appropriate contributors and ensure they have the correct access permissions.

### Create an Informative README.md

- [ ] Include a _Description_ of the software/data in the repository and the AAGI project to which it is linked.
- [ ] Include _Install Instructions_ for how to install the software or load the data (and dependencies!).
- [ ] Include _Usage Examples_ to show end-users how to use your software/data.
- [ ] Include and/or link to the _Licence_ (or if _No Licence_, include a declaration and explanation).
- [ ] Include and/or link to the _Contribution Instructions_ for how people can get involved.
- [ ] Include _Citation and Acknowledgement Information_, as relevant.
- [ ] (Optional) Include repository badges to show build status, version information, and other metrics.

### Determine Your Licencing and Sharing Requirements

- [ ] Consult with collaborators and the GRDC Manager to decide the licence and sharing conditions.
- [ ] Verify that your choice of licence is compatible with any bundled dependencies.
    - **For software repositories:**
    - [ ] Include a licence such as the MIT or GNU GPLv3 (or declare No Licence).
    - **For data repositories:**
    - [ ] Include a licence such as the CC-BY 4.0 or CC-BY-SA 4.0 (or declare No Licence).
    - [ ] Upload dataset metadata to the GRDC Data Catalogue, if required.
    - **For document repositories:**
    - [ ] Include a licence such as the CC-BY 4.0 or CC-BY-SA 4.0 (or declare No Licence).

### (Optional) Do You Need Any Other Repository Files?
- [ ] A .gitignore file, configured appropriately for your repository.
- [ ] A CONTRIBUTING file, that outlines how others can contribute to the repository development.
- [ ] A CODE_OF_CONDUCT.md file that explains the expected standards of behaviour.
- [ ] A SECURITY.md file, outlining your repository’s security and vulnerability reporting procedures.

### Set Up Your Branches
- [ ] Set up _main_ branch (stable, production-ready) and configure branch protection rules if needed.
- [ ] (Optional) Set up _dev_ branch (ongoing development) and configure branch protection rules if needed.
- [ ] (Optional, recommended for larger repositories) Set up additional branches for features and bug fixes.

## 2. Ongoing Repository Compliance

The following checklist items help you to make sure that your AAGI-AUS repository is maintaining adherence to AAGI’s professional standards for documentation, publishing and collaborator conduct. It is recommended that you revisit these items regularly, and especially before you make any new public version releases.

### Basic Repository Compliance
- [ ] Is your repository _public_? (If it is _private_, can it be made publicly accessible yet?)
- [ ] Are the title and brief description for the repository still accurate and appropriate?
- [ ] Does the README contain adequate and current information about the software/data?
- [ ] Do the README installation instructions and usage examples still work, or do they need to be updated?
- [ ] Is the repository licenced? (And if not, is this adequately stated and explained in the README?)
- [ ] Are there any visible problems, such as failed deployments or broken images/badges?

### Conduct and Management Compliance
- [ ] Is it clear from the README/CONTRIBUTING file how to get involved in the development?
- [ ] Are there any outdated or abandoned branches that should be deleted?
- [ ] Is your branching strategy (still) appropriate to the size of your software/data and contributor team?
- [ ] Are you and your collaborators using disciplined versioning (e.g., MAJOR.MINOR.PATCH)?
- [ ] Are there any open issues that have not be resolved, discussed or assigned to a contributor?

### Security Compliance
- [ ] Are there any contributors that no longer require elevated permissions in the repository?
- [ ] Is the repository unreasonably large (≥5GB), or does it contain any unreasonably large files (≥50MB)?
- [ ] Are there any superfluous files (such as output files from compilation) that can be removed?
- [ ] _Has any sensitive information (such as PII, credentials, or API keys) been uploaded to the repository?_[^1]

[^1]: If sensitive information has been uploaded to the repository, report this to an AAGI senior software developer immediately.

### Documentation Compliance
- [ ] Is the level of documentation to an appropriate standard, given the repository’s size and purpose?
- [ ] If you have additional documentation such as user manuals or vignettes, are these still up-to-date?
- [ ] Are your software/data files documented to an appropriate standard?
    - **For software scripts:**
    - [ ] Do scripts contain, at minimum: a description, author, and date at the top?
    - [ ] Are longer scripts (≥100 lines) commented appropriately to help others use/understand them?
    - **For (small) software libraries and packages:**
    - [ ] Are your functions, classes and datasets documented to an appropriate degree?
    - **For large software libraries, packages and applications:**
    - [ ] Have all functions, classes, modules and datasets been documented comprehensively?
    - [ ] Are you using automated generators (Roxygen, Sphinx) to create useful documentation for users?
    - [ ] Are you using a testing framework with an appropriate level of test coverage?
    - [ ] Are you using continuous integration/deployment practices, and do these work without error?
    - [ ] Do you have an appropriate level of ancillary documentation to aid with contributor onboarding?
    - [ ] If you are using subcomponents or bundling libraries, are the licences for these compatible?
    - **For datasets:**
    - [ ] Have you included metadata descriptions with an appropriate level of detail?
