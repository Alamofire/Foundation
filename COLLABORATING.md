# Collaboration Tools and Workflows

This document is intended for internal use by the Alamofire Technical Committee (TC). It documents how we use various tools and workflows to communicate and manage the individual projects. The collaboration workflows for the following tools are documented below.

* [GitHub](#GitHub)
* [Trello](#trello)
* [Slack](#slack)

---

## GitHub

GitHub will be used for tracking public issues as well as community and internal pull requests. If an issue is opened on GitHub, then it should be labeled and addressed directly on GitHub. If the issue requires internal discussion, then that discussion should take place in Slack. If the item is going to require internal development, then the issue should move to Trello. While the issue is in development in Trello, the GitHub issue should be kept up-to-date to keep the community in the loop.

### Labels

With the amount of issues typically logged in large, open-source projects by the community, it is imperative to define a labeling system to help the TC categorize them quickly.

#### Main Labels

The main labels represent all those vital to running a large project. Each label contains a description to clarify when it should be used.

> `Alamofire` is mentioned in several label descriptions and is intended to represent all projects supported underneath the Alamofire Software Foundation.

| **Label**  | **Description** |
| ------------- | ------------- |
| `bug`  | Issue related to a defect on any public branch and/or tag.  |
| `support`  | Issue that belongs on [Stack Overflow](http://stackoverflow.com) where the user needs help using Alamofire. This would serve two purposes 1) to track how many of these types of issues are being filed incorrectly 2) as a way to publicly shame those filing tickets incorrectly. You don't want your issue to receive a `support` label from the TC. |
| `question`  | Issue inquiring about the design or implementation details of Alamofire directed towards the TC. These issues are not looking for support, but instead information that only the TC can answer or speak to. Some of these issues will most likely lead to bug, enhancement or feature request issues. |
| `feature request`  | Issue requesting a new feature be added. |
| `enhancement`  | Issue requesting that a current feature be enhanced. |
| `duplicate` | Issue is a duplicate of another issue and should be closed as such. |
| `wont fix` | Issue won't be fixed by the TC. |
| `help wanted` | Issue needs help from the community to be completed. |
| `needs feedback` | Issue needs feedback from the TC. |
| `needs investigation` | Issue needs investigation by the TC. |
| `needs tests` | Issue needs additional tests written around a particular feature or use case. |
| `behaves correctly` | Issue behaves as it was originally designed. |
| `blocked` | Issue is blocked by another issue. |

#### Alamofire Feature Labels

These labels are only intended for `AFNetworking` and `Alamofire`. They represent the high level features and sections of both projects. Other projects inside the Alamofire Foundation should create their own set of feature labels tailored to that project.

**Features**

* `security` 
* `parameter encoding`
* `http headers`
* `multipart form data`
* `response validation`
* `response serializers`
* `upload request`
* `download request`
* `url session`
* `session delegate`
* `async operation`

**Project and Deployment**

* `documentation`
* `carthage`
* `cocoapods`
* `tests`
* `project config`

#### TC Labels

The TC labels allow issues to be tracked for upcoming TC meetings to help with planning the agenda. For more details, please refer to the Alamofire [Goverance](https://GitHub.com/Alamofire/Foundation/blob/master/GOVERNANCE.md).

| **Label**  | **Description** |
| ------------- | ------------- |
| `tc agenda`  | Issue added to the the agenda for the next TC meeting. Community members and collaborators can request an issue be added to the TC agenda by opening a GitHub issue. |
| `tc meeting`  | Issue contains all info about the next meeting including time, public YouTube feed, invitee list and agenda items. |

### Milestones

Milestones should be used in GitHub to track public facing issues and pull requests. This will help make it clear for the public that particular issues and changes are tied to actual releases being internally tracked in Trello. This will result in a bit of duplication with Trello, but it gives the community more visibility into the future direction of the project.

We should create the milestones for each project with high level bullet points of the features we intend to include in the release. Using this approach, feature bullets should only be included in the MAJOR and MINOR releases. PATCH releases should be limited to community issues, pull requests and minor changes being tracked by the TC in Trello.

---

## Trello

Trello is used to track all the internal projects, issues and tasks related to the Alamofire Software Foundation. Each project should have its own board along with lists customized for that particular project. It is up to each project to determine what type of list structure works best.

The Trello board for a particular project should serve as the source of truth for that project. All issues and milestones should be tracked in Trello to ensure nothing gets dropped. If the card also has a public facing issue or pull request associated with it, it should be linked in the Trello card.

### Lists

Organizing the lists for a particular board needs to be thought through carefully. It should be tailored to that particular project to make it easiest to track the status of the project toward a common goal (e.g. a Milestone). There is no one-size-fits-all solution to list structures, but here is a quick example.

| **1.1 Roadmap** | **1.0 ToDo** | **1.0 In-Dev** | **1.0 Done** | **Icebox**      |
| --------------- | ------------ | -------------- | ------------ | --------------- |
| 1.1 card 1      | 1.0 card 7   | 1.0 card 4     | 1.0 card 1   | Cool New Idea 1 |
| 1.1 card 2      | 1.0 card 8   | 1.0 card 5     | 1.0 card 2   | Cool New Idea 2 |
| 1.1 card 3      | 1.0 card 9   | 1.0 card 6     | 1.0 card 3   | Cool New Idea 3 |

Once a particular list or set of lists are completed, they can be archived to make room for the next set. You can easily re-open archived lists if necessary.

### Cards

Cards in Trello can represent almost anything. Regardless of whether it represents a feature, story, task, discussion, etc., it needs to contain enough information so everyone in the project understands the requirements of the card. It should contain the appropriate amount of detail as well as the necessary labels to make it easy for everyone to quickly understand when and why a card needs attention. It is also encouraged to use the `Due Date` feature of a card when we're working towards a particular release on a project.

### Labels

Since all cards are created internally by the TC and collaborators, it is best to maintain a small, focused set of labels designed to meet the needs of a particular project. The following labels are merely suggestive in nature. Always ensure each project is maintained with the minimal amount of process to ship the highest quality software possible.

#### Common Labels

* `feature`
* `enhancement`
* `documentation`
* `task`
* `bug`
* `blocked`
* `needs feedback`
* `needs investigation`

#### Assignee Labels

* `christian`
* `kevin`
* `kyle`
* `mattt`
* `unassigned`

### Milestones

Milestones for a project should be tracked in a list. The cards should be placed into the appropriate milestone list. If you're unsure which milestone the card belongs in, it should be placed in the `Icebox`. We can then discuss items in the `Icebox` during a TC meeting to determine what exactly to do with them.

There are going to be some cards which are already listed in a public issue on GitHub or an issue that we need feedback on from the community. Those cards should be duplicated on GitHub and any public info that we'd like to share should be duplicated in GitHub. Trello cards should always serve as the "source of truth" for an issue.

---

## Slack

Slack is a fantastic communication tool for quickly discussing an issue or feature as a group. When a particular issue, feature or question arises, Slack is the fastest way to reach a resolution as a group. With that said, it is important to document the resolution in the appropriate tool such as GitHub or Trello. Searching through Slack for a particular conversation several weeks ago can prove challenging, especially for those that were not involved in the conversation.