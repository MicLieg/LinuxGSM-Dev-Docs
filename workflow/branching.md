# Pull Requests

Pull requests (PRs) allow reviewers to examine the changes a developer has made to a branch. LinuxGSM uses this method, allowing developers to propose code for review that is either ready or almost ready to being integrated into the `develop` branch.

When the code you have worked on is ready to be submitted to the LinuxGSM project, you will need to create a pull request. Follow these steps closely to ensure that your code can be merged as fast as possible.

## Before a Pull Request is created

Before a Pull Request is created ensure that the code is ready to be merged into the project. This means that the code has been tested, works and is documented. To make this step easier a [Pull Request Template](https://github.com/GameServerManagers/LinuxGSM/blob/master/.github/pull_request_template.md) has been created to guide the submission.

If the PR is not quite ready for merge but is ready for review and feedback ensure the subject of the PR contains `[WIP]` (Work in Progress) and mark the Pull Request as draft.

## Naming a Pull Request

When naming a pull request ensure that it is following [Conventional Commits](https://www.conventionalcommits.org/) standards; as this is what is used for generating the [changelog](https://github.com/GameServerManagers/LinuxGSM/releases) for the next release.

A best practice for writing a commit message is to say in your head the following, followed by the change you are making.

> If I commit this change it will ... _add slack support to alerts_

```bash
feat(alerts): add slack support to alerts
```

```bash
fix(csgoserver): remove SteamCMD auth requirement 32-bit workaround
```

## After a Pull Request is created

Once the Pull Request is created various unit tests are carried out to check that the code follows standards and does not break LinuxGSM. Feedback is given by the tests once they are completed. It's okay if some of the tests fail, you can continue to work on the Pull Request and push new commits to the branch. The tests will run again once the new commits are pushed.

Now it's time to wait.

The Pull Request will need to be reviewed by LinuxGSM developers who regularly work on the project. They will `accept`, `reject` or `recommend changes` to the Pull Request. This can take time or your pull request will be held until a time that is appropriate to merge into the project so please be patient. One of the developers may leave a review to give feedback or make changes themselves to prepare the commit for release. Once this review process is completed congratulations your commit will be merged.

## Merged into develop

Once merged into the develop branch, your code will be tested for compatibility with other existing and new features. When the code is ready for release, it is merged into the master branch, which makes it live.
