# Contributing Guidelines
Thank you for your interest in contributing to the project! By following this guideline, we hope to ensure that your contributions are made smoothly and efficiently.

<!-- TOC -->
1. [Suggesting Improvements](#suggesting-improvements)
2. [Contributing Code](#contributing-code)
3. [Contributing Documentation](#contributing-documentation)
<!-- /TOC -->

## Suggesting Improvements
Great you wish to help improve the project either with an idea, problem, or documentation change you have come up with. To do this, you will need to raise a [new issue](https://github.com/HillSheepStudios/factory-diagnostics/issues/new/choose), and then select one of three issue types.

<!-- TOC1 -->
- [Report a Problem](#report-a-problem)
- [Suggest a Behaviour Change](#suggest-a-behaviour-change)
- [Report a Vulnerability](#report-a-vulnerability)
<!-- /TOC1 -->

### Report a Problem
If you discover a problem with the documentation or codebase, first check the [Issues Backlog][issues-backlog] to see if the issue has already been reported. Use the [Problem Report Template][problem-report] and provide detailed information about the problem, including steps to reproduce it.

### Suggest a Behaviour Change
If you want to suggest a new feature or improvement, first check the [Issues Backlog][issues-backlog] to ensure a similar suggestion hasn't yet been made. Use the [Behaviour Change Request (BCR) Template][BCR] to provide a detailed description of your suggestion.

### Report a Vulnerability
If you identify a security concern, please use the [Report a security vulnerability][security-vulnerability] template to share the details. This report will only be viewable to repository maintainers. You will be credited if the advisory is published.

---


## Contributing Code
Contributing to the codebase is as simple as selecting an issue from the [Issues Backlog][issues-backlog] and submit your changes through a pull request.

<!-- TOC2 -->
- [Code Pre-requisites](#code-prerequisites)
- [Code Guide](#code-guide)
- [Unit Tests](#unit-tests)
- [Integration Tests](#integration-tests)
- [Behaviour Tests](#behaviour-tests)
- [Codebase Pull Request Guidelines](#codebase-pull-request)
<!-- /TOC2 -->

### Code Prerequisites
The following prerequisites are required to contribute to the codebase:

<!-- TODO: Insert the prerequisites as bullet points -->

### Code Guide
All codebase changes must be submitted through a pull request, see the [Pull Request Guidelines][pr-guide] for more information. When making changes to the codebase, consider the following guidelines:

1. **Understand the Codebase**: Before making changes, ensure you understand the part of the codebase you are working on. If you're unsure, ask for help or spend time reading and running the code.
2. **Small Changes**: Make small, incremental commits. This makes your changes easier to understand and review.
3. **Testing**: Ensure your changes are covered by tests. This helps to verify that your changes work as expected and don't break existing functionality.
4. **Documentation**: Update the documentation to reflect your changes. This includes both code comments and external documentation if it exists.
5. **Performance**: Consider the performance implications of your changes. Avoid unnecessary computations, and use efficient algorithms and data structures.
6. **Error Handling**: Handle potential errors gracefully. Your code should not crash or behave unexpectedly when encountering errors.
7. **Compatibility**: Ensure your changes are compatible with the rest of the codebase. Avoid making changes that would require large-scale modifications to other parts of the code.
8. **Commit Messages**: Write clear, concise commit messages that explain your changes. See the [Commit Message Guidelines](./docs/contributors/guide#commit-message) for more details.
9. **Sign-off**: Your commits must be signed off. See the [Sign-off Guidelines](./docs/contributors/guide#commit-sign-off) for more details.
10. **Review and Feedback**: Be open to feedback and willing to make changes based on review comments. Code review is a collaborative process and an opportunity to improve the quality of your code.

See the [Contributors Guide](./docs/contributors/guide) for more information that will aid you in contributing to the codebase.

### Unit Tests
Unit tests are used to verify the smallest piece of code that can be logically isolated. They are written in a way that allows for the codebase to be tested in isolation. Please create or update tests relevant to your changes. Ensure all tests run successfully to verify that your modifications do not adversely affect other functionalities.

Run unit tests:
<!-- TODO: Run unit tests -->
```sh

```

### Integration Tests
Integration tests are tests that validate the interaction between different parts of the system as a whole. They are designed to detect interface defects, inconsistencies between integrated components, and issues with the system's environment or data. These tests are crucial for ensuring that the system functions correctly when all its components are integrated.

Run integration tests:
<!-- TODO: Run integration tests -->
```sh

```

### Behaviour Tests
Behaviour tests are used to validate that the system behaves as expected in various scenarios. They are written from the user's perspective and help to ensure that all functionalities of the system work correctly under different use cases. These tests are crucial for verifying that the system meets the user's requirements and expectations.

Run behaviour tests:
<!-- TODO: Run behaviour tests -->
```sh

```

### Codebase Pull Request
When creating a pull request, consider reading the [Pull Request Guide][pr-guide] before submitting a pull request. For a pull request to be accepted, it must meet the following criteria:

- Ensure PR message aligns with [Pull Request message guidelines](./docs/contributors/guide#pull-request-message) for the project.
- Your PR must be signed off. See the [Sign-off Guidelines](./docs/contributors/guide#commit-sign-off) for more details.
- Automated checks all pass. See the [Automated Pull Request Checks](./docs/contributors/guide#automated-pr-checks) section for more information.
- Maintainers have successfully reviewed the pull request.

The factory won't merge your changes until it has the tests passing against the *current* `HEAD` of `main` - but don't worry, whilst the tests *continue* to pass it will automatically merge your pull request into main and rerun the tests. As you can imagine, this can take a little while if the merge queue is long. 
Full details can be found in the [Pull Request Submit Process](./docs/contributors/guide#pull-request-process) guide.

---


## Contributing Documentation
Contributing to the codebase is as simple as selecting an issue from the [Issues Backlog][issues-backlog] and submit your changes through a pull request.

<!-- TOC3 -->
- [Documentation Pre-requisites](#documentation-prerequisites)
- [Documentation Guide](#documentation-guide)
- [Documentation Pull Request Guidelines](#documentation-pull-request)
<!-- /TOC3 -->

### Documentation Prerequisites
The following prerequisites are required to contribute to the documentation:

<!-- TODO: Insert the prerequisites as bullet points -->

### Documentation Guide
All documentation changes must be submitted through a pull request, see the [Pull Request Guidelines][pr-guide] for more information. When making changes to the documentation, please follow these guidelines:

1. **Accuracy**: Ensure that the documentation is accurate. The information should correctly describe the current state of the system.  
2. **Clarity**: The documentation should be clear and easy to understand. Avoid jargon and complex sentences.  
3. **Completeness**: The documentation should be complete. It should cover all aspects of the system and not leave out important details.  
4. **Consistency**: The documentation should be consistent. Use the same terminology, style, and format throughout the documentation.  
5. **Grammar and Spelling**: Check the documentation for spelling and grammar errors. These can make the documentation harder to understand.  
6. **Formatting**: Use formatting to make the documentation easier to read. This includes using headings, lists, code blocks, and other Markdown features.  
7. **Links and References**: Ensure that all links and references in the documentation are valid and lead to the correct places.  
8. **Images**: If the documentation includes images, ensure that they are clear, relevant, and include alt text for accessibility.  
9. **Code Snippets**: If the documentation includes code snippets, ensure that they are correct and useful. Consider including a reference to a full example if possible.

### Documentation Pull Request
When creating a pull request, consider reading the [Pull Request Guide][pr-guide] before submitting a pull request. For a pull request to be accepted, it must meet the following criteria:

- Ensure PR message aligns with [Pull Request message guidelines](./docs/contributors/guide#pull-request-message) for the project.
- Your PR must be signed off. See the [Sign-off Guidelines](./docs/contributors/guide#commit-sign-off) for more details.
- Automated checks all pass. See the [Automated Pull Request Checks](./docs/contributors/guide#automated-pr-checks) section for more information.
- Maintainers have successfully reviewed the pull request.

The factory won't merge your changes until it has the tests passing against the *current* `HEAD` of `main` - but don't worry, whilst the tests *continue* to pass it will automatically merge your pull request into main and rerun the tests. As you can imagine, this can take a little while if the merge queue is long.
Full details can be found in the [Pull Request Submit Process](./docs/contributors/guide#pull-request-process) guide.

---

[pr-guide]: ./docs/contributors/guide#pull-request-guidelines
[issues-backlog]: https://github.com/HillSheepStudios/factory-diagnostics/issues
[problem-report]: https://github.com/HillSheepStudios/factory-diagnostics/issues/new?template=problem_report.md
[BI]: https://github.com/HillSheepStudios/factory-diagnostics/issues/new?template=behaviour_increment.md
[security-vulnerability]: https://github.com/HillSheepStudios/factory-diagnostics/security/advisories/new
