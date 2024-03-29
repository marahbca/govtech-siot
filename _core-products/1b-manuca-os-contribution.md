---
layout: leftnav-page-content
title: Contributing
permalink: /core-products/manuca/manuca-os-contribution/
breadcrumb: MANUCA - Contributing
second_nav_title: "MANUCA"
collection_name: core-products
---

# Contributing to MANUCA OS

MANUCA OS is an open-sourced RTOS that is designed to work with the MANUCA DK. Contributions are an important part of the MANUCA ecosystem, and the wider Singapore Government Tech Stack. Our goal is to make it as simple as possible to become a contributor.

You can make contributions to the source code hosted on GitHub. All contributions will be bounded by an Apache License version 2.0 (Apache-2.0).

To encourage collaboration, as well as robust, consistent and maintainable code, we have built a set of guidelines for contributing to MANUCA OS.

## How to contribute

MANUCA OS has a team of maintainers ([@lauleehong](https://github.com/lauleehong), [@ziqiyap](https://github.com/ziqiyap), [@gohkokboon](https://github.com/gohkokboon)). This team is responsible for helping you get your changes in, as well as controlling the overall quality and consistency of the software.

We accept contributions in the form of pull requests. Each pull request must be reviewed by at least one other developer experienced with the functionality. For contributions that span multiple functionalities, multiple reviewers may be necessary. After reviews are complete, we test the changes as part of a larger system. The testing includes but is not limited to: functional correctness, integration with other parts of the system, code style or formatting and regressions, such as code size increase or performance degredation. If any of the tests fail, more work will be needed before we accept the contribution.

All functions and methods must include a corresponding doxygen-styled API documentation header in the souce code.

## Types of contributions

1. **Bugfix**
   - A bug fix is a change that fixes a specific defect in the codebase with backward compatibility. These are the highest priority because of the positive effect the change will have on users developing against the same code. A bug fix should be limited to restoring the documented or proven otherwise, originally intended behavior. Every bug fix should contain a test to verify results before and after the pull request. Bug fixes are candidates for patch releases.
   - Create branch with the prefix `bugfix/`. For example bugfix/foo-bar
2. **Feature**
   - A feature can be any change in the functionality, including adding a new feature, a new method or a function. A feature contribution contains a new API, capability or behavior. It does not break backward compatibility with existing APIs, capabilities or behaviors. New features should also come with documentation and comprehensive test coverage. Feature PRs are treated cautiously, and new features require a new minor version for the codebase. Features are candidates for feature releases.
   - Create branch with the prefix `feature/`. For example feature/foo-bar
3. **Others**
   - All other types of pull request not convered above will fall into this category. This includes pull requests for docmentations, code refactoring and updating of unit tests. Depending on the impact of the change, this branch may be queued to a lower priority.
   - Create branch with the prefix `others/`. For example others/foo-bar

## GitHub Pull Request Workflow

![PR Flowchart](/images/manuca/intro/manuca_os_github_pr_sm.png)
