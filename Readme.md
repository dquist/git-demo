# Git Overview

## Discussion Topics

- Git Jargon and Uses
- Master
- Fork
- Branch
- Pull Request
- Typical Workflow
- Bug/improvement introduction to committed changes
- Hurdles we may experience transitioning from a familiarity with TFS and TortoiseSVN

## Biggest Differences between Git and TFS

- Distributed vs centralized
  - Commit changes locally, synchronize with server
  - Incredibly powerful, but most confusing
- Multiple Git Server options
  - GitHub
  - Azure DevOps
  - GitLab (SaaS or self-hosted)
- Lightweight branching.
  - Branches can be created instantly
  - Easily switch between master and feature branches
  - Typical to have many local branches 
  - Branches are local by default, need to explicitly share
- Powerful merging and rebase capabilities 
  - Upstream changes from mainline can be auto-merged
  - Using diff tool (like BC) only required for conflicts
- Command-line based (can still use UI)

## Typical workflow

- Synchronize local workspace with remote using `git pull`
- Create a new feature branch. `git checkout -b dan/feature-1`
- Make changes in your local workspace
- Commit changes locally using `git commit`
- Push branch to remote server
- Create a Pull Request (Merge Request) to merge into master


## Recommendations

- Invest in training
- Take time to understand core concepts. Cannot stress this enough.
- Use pull requests for code reviews
- Avoid long-lived feature branches
  - Merge early and often
  - Simplifies code reviews
  - Reduces conflicts
- Use Continuous Integration (CI) tools to verify builds before merging into master
- Define an organizational branching strategy
  - Lots of recommendations out there
  - Dan's advice - keep it simple
    - master - Latest changes
    - features - short-lived branches for new features and bug fixes
    - releases - Each public release gets a dedicated branch for hotfixes (ex: `release-1.1`)

