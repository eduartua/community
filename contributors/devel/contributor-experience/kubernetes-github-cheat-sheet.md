# Kubernetes Github Magic
This document has information that you are not going to find in any other document in the Kubernetes org repositories. The majority is considered a group of tips and tricks which cover common project/git practices, and you can see it as a TL;DR. They will be beneficial to your aha! moment.

**Table of Contents**
- [Communicating Effectively](#communicating-effectively-on-github)
  - [How to be excellent to each other](#how-to-be-excellent-to-each-other)
    - [Examples of good/bad communication](#examples-of-good/bad-communication)
- [Submitting a contribution](#submitting-a-contribution)
  - [Opening a issue](#opening-an-issue)
  - [Opening a pull request](#opening-a-pull-request)
    - [Pull requests advantages](#pull-requests-advantages)
  - [Example of first comments when opening an issue or a PR](#example-of-first-comment-when-opening-an-issue-or-a-pr)
  - [About trivial fixes](#about-trivial-fixes)
  - [Working locally](#working-locally)
    - [Branches](#branches)
    - [Squashing Commits](#squashing-commits)

## Communicating effectively on Github

### How to be excellent to each other
First, read the [Code of Conduct]

#### Examples of good/bad communication
  🙂 “X doesn’t compile when I do Y”  
  😞 “X doesn’t work! Please fix it!”

  When closing a PR we should convey an explanatory and cordial message talking about why it does not meet the requirements to merge it. It may offer feedback.  
  **Example:**

  🙂 “I’m closing this PR because this feature can’t support the use case X, but as you’ve propoused it can be a great idea to implement in Y tool. Thanks for  working on this.”

  😞 “Why isn’t this following the api conventions? This is a complete failure!”

## Submitting a Contribution

### Opening an issue
Issues help you in any of the following situations:
There is something that doesn’t work as expected or keep throwing errors.
Open a discussion about an improvement or a high-level idea.
Propose new enhancements or features.

Examples of excellent communication on issues:
  - When tackling an issue, let people know that you are working on it to avoid duplicate work. This can be done commenting on the issue.

  - When you have resolved something on your own at any future time, comment on the issue letting people know before closing it.

  - Always use references about others PRs or issues. It is useful to identify that something has been addressed somewhere else.
	
### Opening a pull request
Pull requests are useful in the following scenario:
- You have done trivial fixes; that is broken links, typos, grammar mistakes and anything that is a clearly identifiable error.
- You have done fixes to a contribution that has already been discussed on an issue.

#### Pull requests advantages
- Maintainers and contributors give feedback when commenting pull requests.
- It can be labeled as “Work In Progress” if you’ll add more commits later.
- They don’t represent a finished work.
- If something is wrong about a PR, and a conflict that can harm the project integrity is identified, you can close it without affecting the project - itself.

### Example of first comment when opening an issue or a PR:
```
Ref. #3064 #3097
All files owned by SIG testing were moved from /devel to the new folder /devel/sig-testing.
/sig contributor-experience
/cc @parispittman @nikhita
/kind cleanup
/area developer-guide
/assign @cblecker @spiffxp @timothysc
```
		
#### What’s in that comment?
  - Reference to another issues or PRs (#3064 #3097).
  - A brief description of what’s done.
  - SIG assignation with the command /sig contributor-experience. Learn more about [commands] and about [SIGs].
  - Reviewers that may have interest on this specific issue or PR are specified with the /cc command.
  - The /kind cleanup command add a label that categorizes issue or PR as related to cleaning up code, process, or technical debt. Learn more about [labels].
  - The /area developer-guide command categorizes issue or PR as related to the developer guide.
  - The command /assign assigns an assignee to the PR. Usually the file OWNER who will add the /approve label to the pull request.

### Reopening PRs
There are moments where PRs can take longer than you may expect. Therefore, if no reviewer picked up on it within a day or so, it is suggested that you'd close the PR and reopen a new one / reassign to a different person.

### Issue labels
Labels are the way Kubernetes issues are identified. This [labels.md] file has a list of all labels that can be applied to all repos.

#### What is a good Github issue label?
Good issue labels help to manage issues efficiently. Some important labels that you can use to start you PR are:
  - `/sig SIG_NAME` This one helps to assign a proper SIG for the ownership of the issue.
  - `/area AREA_NAME` This is used to associate issues or PRs to a specific area.
  - `/kind CATEGORY` This labels helps to categorize the issue.

### About trivial fixes
Trivial fixes or edits are always the best candidates for new contributors, and we believe this is a smooth way to introduce them to any subproject in the Kubernetes organization. However, it is more beneficial if we take the entire document which we are working with and give it a full review. One of the main benefits of this is to have just one PR with most the the changes regarding typos. Learn more about [trivial] fixes.

### Working locally
#### Branches
Branches are you best friends when working locally. It is suggested to  create new branches to add new code. To create a new branch run:

`git checkout -b myfeature`

Learn more about the [Github workflow and branching].

#### Squashing Commits
The main purpose of squashing commits is to have a good readability of the git history. Grouping certain changes together before sharing allow us to have a very clean and easy to read documentation of the changes done. Usually this is done in last phase of a PR revision. Learn more about [squashing commits].


[code of conduct]: https://github.com/kubernetes/community/tree/master/committee-code-of-conduct
[commands]: https://prow.k8s.io/command-help
[SIGs]: https://github.com/kubernetes/community/blob/master/sig-list.md
[labels]: https://github.com/kubernetes/test-infra/blob/master/label_sync/labels.md
[trivial]: http://git.k8s.io/community/contributors/guide/pull-requests.md#10-trivial-edits
[Github workflow and branching]: https://github.com/kubernetes/community/blob/master/contributors/guide/github-workflow.md#3-branch
[squashing commits]: https://github.com/kubernetes/community/blob/master/contributors/guide/pull-requests.md#6-squashing-and-commit-titles
[labels.md]: https://github.com/kubernetes/test-infra/blob/master/label_sync/labels.md