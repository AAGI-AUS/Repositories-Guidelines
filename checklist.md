# AAGI-AUS GitHub Repository Setup Checklist

## Essential Repository Setup
- [ ] Choose a descriptive repository name following AAGI naming conventions
- [ ] Set repository visibility (public unless there's a specific reason for privacy)
- [ ] Add appropriate team members with correct access permissions

## Required Files
- [ ] Create a comprehensive README.md with:
  - [ ] Project title and description
  - [ ] Installation instructions
  - [ ] Usage examples
  - [ ] License information
- [ ] Add LICENSE file (after consultation with GRDC)
  - [ ] For code: MIT License (preferred), GPL v3, or Apache 2.0
  - [ ] For data: CC-BY 4.0 or CC-BY-SA 4.0
  - [ ] For documentation: CC-BY 4.0

## Recommended Additional Files
- [ ] CONTRIBUTING.md file explaining how others can contribute
- [ ] CODE_OF_CONDUCT.md outlining expected behavior
- [ ] .gitignore file configured for your project type

## Branch Structure
- [ ] Set up main branch (stable, production-ready code)
- [ ] Create develop branch for ongoing development (if needed)
- [ ] Configure branch protection rules for critical branches

## Documentation
- [ ] Document code with consistent style (functions, parameters, returns, examples)
- [ ] Include badges for build status, coverage, etc. (if applicable)
- [ ] Document dependencies and requirements
- [ ] Add citation information (if applicable)

## Version Control Practices
- [ ] Follow semantic versioning (MAJOR.MINOR.PATCH)
- [ ] Set up issue templates for bugs, features, etc.
- [ ] Configure pull request templates

## Special Considerations
- [ ] Consult GRDC before making any code or data public
- [ ] For data repositories: plan to upload CC-licensed data to GRDC Data Catalogue
- [ ] For large files: set up Git LFS or external storage solution
- [ ] Ensure no sensitive information is committed (credentials, API keys, etc.)

## Pre-Launch Verification
- [ ] Verify license compatibility with dependencies
- [ ] Check that documentation is complete and accurate
- [ ] Ensure any institutional or funder requirements are met