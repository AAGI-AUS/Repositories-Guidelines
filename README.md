- [Introduction](#introduction)
- [Repository Requirements](#repository-requirements)
- [Types of Repositories](#types-of-repositories)
  - [Other Recommended General Repository Contents](#other-recommended-general-repository-contents)
- [Repository Settings and GitHub Organisation settings](#repository-settings-and-github-organisation-settings)
- [Documentation Standards](#documentation-standards)
  - [README.md Content](#readmemd-content)
  - [Code Documentation](#code-documentation)
- [Licencing](#licencing)
  - [Summary](#summary)
  - [Recommended Licences](#recommended-licences)
    - [For Code Repositories](#for-code-repositories)
    - [For Data Repositories](#for-data-repositories)
    - [For Documentation](#for-documentation)
  - [When to Use Each Licence](#when-to-use-each-licence)
  - [Licence Compatibility Considerations](#licence-compatibility-considerations)
  - [Adding a License to Your Repository](#adding-a-license-to-your-repository)
  - [Special Considerations](#special-considerations)
- [Version Control Practices](#version-control-practices)
  - [Branching Strategy](#branching-strategy)
  - [Commit Guidelines](#commit-guidelines)
    - [Commit Messages](#commit-messages)
    - [Commit Practices](#commit-practices)
  - [Documenting and Replying to Issues](#documenting-and-replying-to-issues)
    - [Creating Issues](#creating-issues)
    - [Replying to Issues](#replying-to-issues)
  - [Pull Requests and Reviews](#pull-requests-and-reviews)
    - [Creating Pull Requests](#creating-pull-requests)
    - [PR Template](#pr-template)
    - [Code Review Process](#code-review-process)
    - [Merging Guidelines](#merging-guidelines)
  - [Tagging and Release Management](#tagging-and-release-management)
  - [Resolving Conflicts](#resolving-conflicts)


# Introduction

These guidelines aim to establish best practices for managing GitHub repositories within the AAGI-AUS GitHub organisation. By following these standards, we ensure our work is reproducible, well-documented, and accessible to colleagues and collaborators. While these guidelines are language-agnostic, they incorporate principles from [rOpenSci](https://devguide.ropensci.org/) where relevant.

See the [AAGI-AUS GitHub Repository Setup Checklist](/checklist.md) for a summary of the essential repository setup.

# Repository Requirements

- Repositories need a name. The name should be descriptive and follow the naming conventions of the AAGI organisation. This may be a project name or an output name such as a package or pipeline.
- Where applicable, repositories need a license. See the [licencing](#licencing) section for more information.
- Repositories should have a README file that provides an overview of the project, how to install it, and how to use it.

# Types of Repositories
Most of the AAGI-AUS repositories will fall into one of the following categories:
- **Code Repositories**: These contain code for software, libraries, or tools. They should include a README, license, and documentation.
- **Data Repositories**: These contain datasets, including raw data, processed data, and metadata. They should include a README, license, and documentation.
- **Documentation Repositories**: These contain documentation for code or data, or may be presentations or similar. They should include a README, license, and documentation.

> Note: These types are independent of the coding language used. 

## Other Recommended General Repository Contents

- A CONTRIBUTING file outlines how others can contribute to the project.
- A CODE_OF_CONDUCT.md file explains expected behaviour for contributors. We recommend adopting the [Contributor Covenant](https://www.contributor-covenant.org/), which is widely-used across open source projects and establishes clear standards for respectful collaboration.
- A SECURITY.md file that explains the security policy, vulnerability reporting procedures, and disclosure process. This is especially important for repositories with data or authentication features.

# Repository Settings and GitHub Organisation settings
- Repositories should be set to public unless there is a specific reason to keep them private (for example they contain sensitive data or code or are in development)
- The AAGI-AUS GitHub organisation uses 'Teams' to manage access to repositories. Team members can be added to the appropriate teams.


# Documentation Standards
## README.md Content

The README should include:

- Project Title and Description: Clear explanation of the project purpose
- Badges: Build status, code coverage, etc.*
- Installation Instructions: Step-by-step guide to set up the project
- Usage Examples: Basic examples showing how to use the code
- Dependencies: Required software and packages*
- Contributing Guidelines: Link to CONTRIBUTING.md*
- Citation Information: How to cite the project*
- License: Brief license information with link to LICENSE file*

\* Optional/if applicable

## Code Documentation

Use a consistent documentation style appropriate for your language. Document functions, classes, and methods with:

- Purpose description
- Parameter descriptions
- Return/output value descriptions
- Examples when helpful

# Licencing

Choosing an appropriate license for your repository is essential to clarify how others can use, modify, and distribute your work. All repositories should include a LICENSE file in the root directory.

## Summary

- Try to use a permissive license (e.g., MIT, Apache 2.0) for code and data repositories where possible.
- GRDC needs to be consulted before any code or data is made public.
- Leave your repository unlicenced until an appropriate discussion has been had with all parties (often including GRDC manager for the investment).
- Data that is CC-licenced should also be uploaded to the GRDC Data Catalogue and there should be a corresponding dataset line in the IPPO.

## Recommended Licences

For more detail about licences, please refer to https://choosealicense.com/. For our organization, we recommend the following licenses depending on the nature of your project:

### For Code Repositories
- **MIT License**: Simple and permissive, allowing others to use your code with minimal restrictions while still providing attribution. Many of the existing AAGI-AUS repositories use this license.
- **GNU General Public License (GPL) v3**: Ensures that derivative works remain open source with the same license terms.
- **Apache License 2.0**: Similar to MIT but with explicit patent grants and contribution terms.

### For Data Repositories
- **Creative Commons licenses**:
  - **CC-BY 4.0**: Allows reuse with appropriate attribution
  - **CC-BY-SA 4.0**: Allows reuse with attribution, with derivatives sharing the same license

### For Documentation
- **CC-BY 4.0**: Preferred for most documentation
- Consider using the same license as your code for consistency

## When to Use Each Licence

- **MIT License**: Best for libraries, tools, and software you want to be widely adopted with minimal restrictions.
- **GPL v3**: Appropriate when you want to ensure all derivatives remain open source.
- **Apache 2.0**: Suitable for larger projects with multiple contributors, especially if patent concerns exist.
- **CC licenses**: Appropriate for datasets, documentation, and educational materials.

## Licence Compatibility Considerations

- Consider dependencies in your project and their licenses to ensure compatibility.
- Be aware of license compatibility when combining code from different sources:
  - MIT and Apache 2.0 are compatible with most other licenses
  - GPL code requires derivative works to also be GPL-licensed
- When incorporating third-party code, ensure you understand and comply with its license terms.
- Document any third-party components and their licenses in your README.

## Adding a License to Your Repository

1. Create a file named `LICENSE` in the root of your repository
2. Include the full text of your chosen license
3. GitHub provides templates for common licenses when creating new files
4. Reference your license in your README.md

## Special Considerations

- **Dual licensing**: Consider dual licensing for specific use cases (e.g., GPL for open source use, commercial license for proprietary applications)
- **Institutional policies**: Check if your institution has specific licensing requirements or preferences
- **Funder requirements**: Some funding bodies mandate specific open-source licenses. 
  - **GRDC**: In the case of AAGI, GRDC usually has at least partial ownership of the code and data produced by AAGI and projects supported by AAGI and should be consulted before any code or data is made public.

# Version Control Practices

Effective version control practices are crucial for collaborative research and development. Following these guidelines will help maintain clear history, facilitate collaboration, and minimize conflicts.

## Branching Strategy

We recommend using a modified version of the GitFlow branching model:

- **main**: Stable, production-ready code. This branch should always be deployable.
- **develop**: Integration branch where features are combined. This branch contains the latest delivered development changes.
- **feature/**: Feature branches should branch off from `develop` and merge back into `develop`.
  - Name convention: `feature/short-description` or `feature/issue-number-description`
- **bugfix/**: For fixing non-critical bugs.
- **hotfix/**: For urgent fixes that need to be applied to the production version. Branch from `main` and merge to both `main` and `develop`.
- **release/**: Preparation branches for releases, allowing for final testing and minor fixes before merging to `main`.

For smaller projects or single-developer repositories, a simplified approach with just `main` and feature branches may suffice.

## Commit Guidelines

### Commit Messages

- Use clear, descriptive commit messages that explain the "why" not just the "what"

### Commit Practices

- Make small, focused commits that address a single issue or feature
- Tag authors in commit messages to give credit*
- Commit frequently to preserve your work and create a detailed project history
- Amend commits or use interactive rebase to fix mistakes before pushing
- Don't commit:
  - Generated files (add to `.gitignore`)
  - Large binary files (consider Git LFS instead)
  - Sensitive information (credentials, API keys, etc.)

\* Optional/if applicable

## Documenting and Replying to Issues
### Creating Issues
- Use issues to track bugs, feature requests, and tasks
- Provide a clear title and description for each issue
- Use labels to categorize issues (e.g., bug, enhancement, question)
- Assign issues to team members for accountability*

\* Optional/if applicable

### Replying to Issues
- Respond promptly to questions and comments
- Use @mentions to notify team members or collaborators
- Keep discussions professional, focused and relevant
- If an issue is not relevant or cannot be resolved, consider closing it with a comment explaining why

## Pull Requests and Reviews

### Creating Pull Requests

- Create a separate branch for each new feature or bug fix
- Reference related issues in the PR description using keywords (e.g., "Closes #123")
- Include enough information in the description for reviewers to understand the changes
- Add relevant labels, assignees, and reviewers

### PR Template

Consider using a PR template with sections such as:
- Purpose of the change
- Changes made
- How to test
- Additional notes or considerations

### Code Review Process

- All code changes should be reviewed by at least one other team member
- Use GitHub's review features to comment on specific lines
- Reviewers should check for:
  - Code correctness and functionality
  - Adherence to style guidelines
  - Adequate test coverage
  - Proper documentation
  - Potential impacts on other parts of the project

### Merging Guidelines

- PRs should pass all automated checks (tests, linting, etc.) before merging
- Use "Squash and merge" for feature branches with multiple small commits
- Use "Merge commit" for significant changes where commit history should be preserved
- Delete branches after merging

## Tagging and Release Management

- Use semantic versioning (MAJOR.MINOR.PATCH) for version numbers
- Create git tags for releases: `git tag -a v1.0.0 -m "Version 1.0.0"`
- Push tags to GitHub: `git push origin --tags`
- Consider automating releases using GitHub Actions

## Resolving Conflicts

- Keep PRs small and focused to minimize conflicts
- Pull from the target branch regularly to stay up-to-date
- When conflicts occur, communicate with other contributors to resolve them
- Consider using visual merge tools for complex conflicts
