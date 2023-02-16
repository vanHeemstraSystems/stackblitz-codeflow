# 300 - Integrating CodeflowApp bot

**CodeflowApp** is a friendly bot, which provides a one-click link that spins up the whole environment for pull requests and issues. No more context-switching or branch-checkouts, just a new browser tab with a full IDE and a dev server running.

## 100 - Pull requests
Once integrated, it will comment on every PR with a link to instantly run and review it:

## 200 - Issues
Whenever an issue is opened, CodeflowApp checks if a [stackblitz.com](http://stackblitz.com/) bug reproduction URL is present in the comment text.

If reproduction URL is present, CodeflowApp will comment with a "Fix this issue" button that allows you to start a new pull request with the bug reproduction mounted in a sibling folder next to your repo directory for live testing:

## 300 - Installing the CodeflowApp Bot
To install the CodeflowApp bot on a repository, you will install it using GitHub UI.

1. Visit [CodeflowApp profile page](https://stackblitz.com/install-github-app).
2. Select the account or organization, as well as the repositories you want the bot to have access to.

-- - If you choose “all in Organization”, CodeflowApp bot will be installed on all repositories in your organization.

-- - Please don't worry - if you change your mind, you can change the bot access or completely disable it!

**TIP**: Installing CodeflowApp ensures every commit to default branch and any pull request branches are pre-cloned for instant bootup times. Your project will run faster on Codeflow.

## 400 - Disabling CodeflowApp Bot

MORE ...

## 500 - Enabling package overrides for issue reproductions

MORE ...

## 600 - 
