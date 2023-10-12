# Documentation Practices
This document outlines the best practices for documenting code, processes, and projects within the Cotheca Project (and all products).

Our goal is to maintain clear, consistent, and accessible documentation for both internal and external audiences. We use the following approaches to achieve it:


## Code Documentation
- ### Code As Documentation
	- Code assumes a major, if not the primary, role as documentation within the Agile context.
	- Considering code as primary documentation DOES NOT exclude the need for supplementary documentation.
	- Acknowledge that declaring code as documentation doesn't automatically make it good documentation.
	- Use meaningful variable and function names to make code self-explanatory.
- ### Docs as Code
	- Treat documentation as code.
	- Integrate documentation practices into your development process.
	- Store documentation in the same repository.
	- Make sure in-code documentation is up-to-date with code changes.
- ### In-Code Documentation
	- Include comments within the code to explain complex logic, algorithms, or non-trivial functions.
	- Document public APIs and interfaces thoroughly with comments to describe their purpose, inputs, outputs, and usage examples.
	- Use a consistent commenting style
		- #### XML Comments (for C#)
			- Utilize XML comments for documenting classes, methods, properties, and other elements in C# code.
			- Provide descriptions, parameter explanations, and return value details in XML comments.
			- Keep descriptions to one sentence as much as possible.
			- Use `<summary>`, `<param>`, `<returns>`, and other XML tags to structure your comments effectively.

		- #### JSDocs (for JavaScript)
			- Employ JSDoc comments for documenting JavaScript functions, methods, and modules.
			- Describe the function's purpose, parameters, return values, and any exceptions it may throw.
			- Keep descriptions to one sentence as much as possible.
			- Use JSDoc tags like `@param`, `@returns`, and `@throws` for clarity.

## README Files

- Create a README.md file at the root of each repository.
- Use the standardized [template for README](https://github.com/cotheca/docs/blob/main/templates/README-template.md) files that includes sections for project description, installation instructions, usage examples, and contribution guidelines.
- Include a table of contents if the README is lengthy.
### General Structure
- #### Project Description
	- Begin with a concise project description that explains the purpose and goals of the repository.
	- Clearly state what the project aims to achieve and its intended audience.
- #### Installation Instructions
	- Provide clear, step-by-step installation instructions, including any dependencies.
	- Offer platform-specific installation guidance when necessary.

- #### Usage Examples
	- Include examples of how to use the project, showcasing common scenarios and features.
	- Provide code snippets, command-line examples, and screenshots where applicable.

- #### Contribution Guidelines
	- Encourage contributions from the community.
	- Explain how others can contribute, including guidelines for submitting issues and pull requests by following the standardized [README template](https://github.com/cotheca/docs/blob/main/templates/README-template.md).
	- Reference the [Cotheca Docs](https://github.com/cotheca/docs) for the general practices followed at Cotheca.

## Version Control and Collaboration

### Git and GitHub
- Keep documentation files, including READMEs, in version control alongside the codebase.
- Leverage GitHub features, such as issues, pull requests, and project boards, for effective collaboration and issue tracking.
- Encourage peer review of documentation changes just like code changes.
- Configure repositories with default templates before pushing code.
- Make sure to follow PR templates structure when submitting Pull Requests.

### Review and Feedback
- Actively seek reviews and feedback on documentation from team members and the community.
- Welcome suggestions and improvements to enhance the quality and clarity of documentation.

## Security Documentation

- Please provide documentation on security best practices and guidelines for each project, specially for security-sensitive projects.
- Provide clear and standard practices for handling sensitive information like:
	- Application Keys
	- Application Client IDs
	- Encryption Certificates (specially private keys)
	- Personal Identifiable Information (PII)


## Thank You
For contributing to Cotheca and for helping us maintain high-quality documentation.
