# Code Review Process by @CodingCrisis

## Goal
Ensure the peer review process is executed in a manner which assures stable quality of work increments and promotes constant improvement.

## Process Steps
If doing Pair/Mob Programming and TDD, skip these steps. Please still consider best practices.
1. [Author] Create a feature branch for your change (following employed branching strategy)
1. [Author] Make the necessary code changes
1. [Author] Ensure Unit Tests are passing (add new if none are available)
1. [Author] Ensure quality is adequate by running a quality check on the branch (using appropriate tool e.g., SonarQube)
1. [Author] Push code to origin repository and create a Pull Request to target branch
1. Select team member(s) proficient in given region to do the review (if in doubt: ask on Team chat, ask PM/SM or bring up on a Daily Standup)
1. [Reviewer] Review the code and comment the PR
1. [Author] Refactor according to comments, update the PR
1. [Reviewer] Re-check the code and approve the PR
1. [Reviewer] Merge the PR to target branch

## Best Practices
### Author:
* Employ pair/mob programming to skip a Code Review altogether
* Do not waste reviewers time - hand out tested and quality checked code
* Annotate code if it is complex
* Verify build of the feature branch (on build server) in case of more complex changes
* "Reset feedback" when pushing a new change to an active PR (vote already made)

### Reviewer:
* Do not review 500+ lines of code at once - split the work
* Quality reviews are the ones that count - take your time if necessary
* Make a brake after an hour of reviewing code - you are not efficient anymore
* Provide solutions, not only remarks
* Be kind to the author, you might be one another time
* Work with the team to build a shared list of common issues 

### Common:
* Try to make the review process interactive - e.g., set up a call to work together in a continues process -> review, fix issues, re-review. This limits context switching, saves time and integrates the Team better. 

## Optional rules to consider 
* Pull Requests are obligatory for all regular changes (when not doing Pair Programming and TDD)
* PR may be skipped for urgent prod issues and one-liners. Code Review is still obligatory
* PR may be partial if doing large enhancements or projects
* It is not allowed to accept your own PRs
* Feature branch should be up to date with target branch, to minimize the risk of merge conflicts (rebase strongly suggested)
* One reviewer is enough for most changes (request two when changes are risky or broad)
* Author uses the autocomplete option in case of simple changes
* Reviewer is responsible for merging code with designated branch if no autocomplete
* If merge conflicts arise, Author is responsible to work with the Reviewer to resolve them
* Reviewer updates PBI/Bug status if no automation in-place
* Make sure PR notifications are visible to team members
