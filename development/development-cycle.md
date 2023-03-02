# Development Cycle
Cotheca implements a hybrid model of Scrum and Kanban to drive development toward achievable objectives. In overall, Scrum practices drive the consistency needed for shipping and structure, while Kanban handles the continuous flow of passive development and fast adaptability.

 1. *Stakeholders* submit items to the Development Board or create issues to report bugs.
 2. Proposed features are stacked in the **New** column of the [Development Board](https://github.com/orgs/cotheca/projects/2) , if the proposed item seems in scope of the overall Cotheca Project, it gets processed into the **Backlog**.
 3. *Contributors* **pick PBI's** to work on from the **Backlog** column.
 4. *Contributors* **branch out or fork out**.
 5. *Contributors* submit their changes via a **Pull Request** (linked to an issue).
 6. *Lead Contributors* **review Pull Requests** and process them into the current sprint iteration.
 7. Pull Requests are **merged into main**.
 8. *Contributors* **apply QA procedures** to verify that changes work as needed.
 9. **Changes are shipped** in the release cycle iteration.


## Needs
Prior to focusing on deliverables, as developers we need to think about development and how to tackle deliverables with a sustainable development strategy and product lifecycles.

In one hand, if all we focus is on delivering development tends to shift towards maintaining and eventually just bug fixing. When pressure to keep a system running and solving end-user reported bugs take over development operations, development ends up in a dead end of bug-fixing. Most development efforts are lost to support tickets and almost no new development progress.

On the other hand, if development efforts focuses on shipping new features or rewriting the existing source, shipping itself becomes compromised due to development iterations. Maintainability and end-user support turns into a headache for both, the end-users and support engineers given that bugs can't be really fixed up since development iterations loose a direct relationship to open issues.

So, what should the focus be? Well, that really depends on the needs.

The main development needs for Cotheca are the following:
 - Truth is that deliverables feel a bit too ambitious and not attainable. Yet.
 - Goals are definitely too broad and abstract.
 - Currently there's not an active developer team on this.
 - Contributors should be a focus point for catching early adopters in order to build an active development team.
 - Contributors should be able to easily implement their needs from the existing code.
 - There's no formal commitment to develop from contributors.
 - There has to be plan for shipping deliverables despite inactive development.
 - Understanding the development practices should not take more than a day.
 - Product deliverables are several small deliverables. Yes, it's a bit meta.
 - Development needs to be scalable at any point.
 - Have a proactive quality assurance strategy.

## Approach
Given the particular requirements for this open source project, the best approach seems to base development operations on a fluid framework but drive it by a structured methodology.

### The Scrum Side
Scrum, by definition, is an iterative methodology for project management. This iterative nature is what Cotheca focuses on for the Scrum Side of things. Development at Cotheca is driven by 2-week sprints. Not for rushing development, but for refining deliverables.

There's no product owners or scrum master per se. However, scrum master tasks are in place.

#### Sprints
Most new feature development tasks are expected to be completed between 2-4 sprints. Quality Assurance tasks are expected to be completed in a single sprint so that it can be released with consistency as detailed in the [release cycle specs](./release-cycle.md).

#### Roles
"Our" version of Scrum cannot implement the standard roles in Scrum, however, we implement the following roles:
 - **Contributor**
 Can be either passive (works at their own pace) or active (participates in the sprint).
 Does any of the following actions:
	 - Participates in contributing into the repository
	 - Participates in QA tasks
 - **Stakeholder**
 Does any of the following actions:
	 - Pitches a product
	 - Uses the product
	 - Proposes features
	 - Reports bugs
 - **Lead Contributor**
 Does the following actions:
	 - Participates in contributing into the repository
	 - Manages the Product Backlog (via the Development Board)
	 - Reviews Pull Requests
	 - Approves or Rejects Pull Requests

#### Ceremonies
There are no usual Scrum "ceremonies," due to the nature of the project. The only recurrent "ceremony" would be the Sprint Board publishing and Sprint Board closure.

### The Kanban Side
Kanban focuses on an open and visual work load representation to keep track of work in progress and milestones. For so, it seems to be a very good match for the needs of the projects and the GitHub tooling.

#### Boards
All of the development process is driven by two boards:

##### Development Board
Contains all potential new features or bug fixes that contributors could work on. However in order to keep  at any time, at their own pace.
See the [Development Board document](./development-board.md) for more details.

##### Sprint Board
This is definitely a weird Scrum-Kanban implementation as it basically serves as the "active" development Product Backlog items that should be completed, extended, escalated, or abandoned during the current sprint using Kanban status and methodologies within a fixed Scrum sprint time allocation (2-weeks).
Please note that PBIs in this board will trump any Pull Request outside the sprint contributors. The Sprints should be more oriented towards Code Reviews and Quality Assurance, but in order to add a sense of commitment, active contributors' work will be posted into the Sprint Board.
See the [Sprint Boards document](./sprint-boards.md) for more details.
