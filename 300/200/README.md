# 200 - Working in Codeflow IDE

## 100 - What is Codeflow IDE?

**Codeflow IDE** is a fully fledged desktop-grade dev environment capable of running your whole workflow - from production-level dev work to reviewing pull requests.

It is designed for enabling you to quickly spin up the entire environment without the hassle of cloning and installing dependencies.

## 200 - Opening GitHub repositories in Codeflow IDE
To open a GitHub repository in Codeflow IDE, swap "github.com" with "pr.new" in the repository URL.

If you are not logged into StackBlitz, while this product is in beta, you will be prompted to login or create a new account.

## 300 - Saving changes
Whenever a file is changed, you will see a white dot next to its tab in the editor.

Moreover, you will also see that dot on the tab in your browser to remind you that you have unsaved changes.

## 400 - Making a PR with Codeflow IDE
Let's add a file to [ilovecodeflow.com](https://github.com/stackblitz/ilovecodeflow.com).

Follow these steps:

1. Open the link in a new tab. In the GitHub URL of the repository, replace ```github.com``` with ```pr.new```.
2. Open the Preview by clicking on the popup notification in the bottom right corner.
3. Introduce some changes - for instance, in the ```/src/pages/LoveNote.astro``` file change the emojis.
4. Verify the changes in the Preview on the right.
5. Depending on your role:
-- - commit the changes by selecting "Source Control" icon in the left vertical navigation bar, clicking "Create & Push Branch", and naming the branch; or
-- - fork the repository.
6. Stage the changes you have made.
7. Write a Commit Message.
8. Click on "Commit & Push" to send the changes to GitHub.
9. Finally, you can submit your pull request by clicking on the "Open New PR" button 🥳 **Note**: If this button does not show, use the button "Create Pull Request" instaed, which is in line with the left-horizontal diver called "SOURCE CONTROL". Hover over the divider to see the "Create Pull Request" button appear.
10. Enter a Title for your Pull Request and provide a Description. Next, press "Create".
11. The number of your Pull Request (e.g. #199) as well as the details will show when opening the menu item "GitHub Pull Request" in the left-hand side menu of the IDE.

## 500 - Reviewing a PR with Codeflow IDE
Let's look at [this suspicious PR](https://github.com/stackblitz/docs/pull/40).

Follow these steps:

1. [Open the link](https://github.com/stackblitz/docs/pull/40) in a new tab. In the GitHub URL of the repository, replace "github.com" with "pr.new".
2. Codeflow IDE will spin up in the "PR Review mode". Open the Preview by clicking on the popup notification in the bottom right corner.
3. Compare suggested changes with the original file. You can also see the edits rendered in the Preview panel if you navigate to the edited page - in this case, the "What is StackBlitz" page.
4. You can add comments by clicking on the "+" icons, read other comments, or start a review.
5. If you no longer want to see the changes in the "PR Review mode", close the relevant files.

## 600 - Using the CodeflowApp bot

**CodeflowApp** is a friendly bot, which provides a one-click link that spins up the whole environment for pull requests and issues. No more context-switching or branch-checkouts, just a new browser tab with a full IDE and a dev server running.

To integrate the bot, please follow the instructions on [Integrating CodeflowApp bot]().

## 700 - Troubleshooting

MORE ...
