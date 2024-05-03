# Configuring a GitHub Repository
This document provides a quick guide of the configuration required on a GitHub repository to implement a standardized workflow that benefit from the development practices at Cotheca.

1. **Create a GitHub repository**

2. **Configure GitHub settings**

	1. **Add branch protection rules**, at least for 'main'
		
		If this sounds unfamiliar, you can check out the GitHub docs steps to [Create a Branch Protection Rule - GitHub Docs](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/managing-a-branch-protection-rule#creating-a-branch-protection-rule)

	2. **Configure issue templates**
		
		Configuring issues templates helps to have a consistent starting point when creating issues for specific purposes like a "bug report" or a "feature request". This helps contributors to get the initial information they need to get started. If this sounds new to you, you can check out the following resources:
		- [Configuring issue templates for your repository - GitHub Docs](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository)
		- [Bug report template - Cotheca Docs](https://github.com/cotheca/docs/blob/main/templates/.github/ISSUE_TEMPLATE/bug_report.md)
		- [Feature request template - Cotheca Docs](https://github.com/cotheca/docs/blob/main/templates/.github/ISSUE_TEMPLATE/feature_request.md)

	3. **Configure issue labels**
		
		Labels helps keep things neat and tidy, specially for managing DevOps, and are an essential part of Project Management. We use a few extra labels to the default GitHub labels, which you can find at [Standard Cotheca Labels - Cotheca Docs](https://github.com/cotheca/docs/tree/main/practices/github/labels.md)

3. **Add standard files to the repository**
	1. **Add a README file** at the root folder
		
		You can use a standard [README template](https://github.com/cotheca/docs/blob/main/templates/README-template.md) we use.

	2. **Add a CONTRIBUTING file** at the root folder
		
		There's a standard [CONTRIBUTING template](https://github.com/cotheca/docs/blob/main/templates/CONTRIBUTING-template.md) available for you

	3. **Add a LICENSE file** at the root folder
		
		Commonly at Cotheca we license our documentation and our code under the [CC-BY-4.0 License](https://github.com/cotheca/docs/blob/main/LICENSE) and the [MIT License](https://choosealicense.com/licenses/mit/) respectively. For your own Open Source projects you might want to take a look to the [The Legal Side of Open Source - Open Source Guides](https://opensource.guide/legal/). If you are working in a private project then do not add a license, see [No License - Choose a License](https://choosealicense.com/no-permission/).

	4. **Add a Pull Request template**
		
		Pretty similar to issue templates, having a standard [Pull Request template](https://github.com/cotheca/docs/blob/main/templates/.github/pull_request_template.md) in place, helps things be more consistent and efficient. Check out the [Creating a pull request template for your repository - GitHub Docs](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/creating-a-pull-request-template-for-your-repository) guide if you need some help.

4. (Optional) **Configure IDEs or editors Git "prune" behaviour**
	
	By default most IDEs and editors don't erase the reference to deleted remote branches. So, even after deleted, you will keep seeing them in your IDE or editor Git-related UIs. Here's a few guides to help you configure a few IDEs and editors:
	
	- [Git - git-prune Documentation (git-scm.com)](https://git-scm.com/docs/git-prune)
	- [Git settings in Visual Studio | Microsoft Learn](https://learn.microsoft.com/en-us/visualstudio/version-control/git-settings?view=vs-2022#prune-remote-branches-during-fetch)
	- [Visual Studio Code November 2020](https://code.visualstudio.com/updates/v1_52#_git-new-settings)
	- [How can I refresh already deleted Git remote branches? – IDEs Support (IntelliJ Platform) | JetBrains](https://intellij-support.jetbrains.com/hc/en-us/community/posts/360006539480-How-can-I-refresh-already-deleted-Git-remote-branches)