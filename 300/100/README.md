# 100 - Using pr.new

Based on "Using pr.new" at https://developer.stackblitz.com/codeflow/using-pr-new

## 100 - What is pr.new?
**pr.new** is a short URL that can be used on any repository to explore code, a branch or an issue, to review a PR, or even to edit a file, all in a live environment with a realtime preview.

## 200 - How does pr.new work?
Behind the scenes, this short URL will choose different tools in different scenarios:

### 100 - Opening a GitHub repository

To open a GitHub repository with **pr.new**, visit it on GitHub and in the browser's address tab, add ```pr.new``` to the beginning of the URL, for example:

[https://pr.new/github.com/stackblitz/docs](https://pr.new/github.com/stackblitz/docs)

Or

[https://pr.new/github.com/vanHeemstraSystems/stackblitz-codeflow](https://pr.new/github.com/vanHeemstraSystems/stackblitz-codeflow)

You will be redirected to [Codeflow IDE](https://developer.stackblitz.com/codeflow/working-in-codeflow-ide) where you can work to [submit a PR](https://developer.stackblitz.com/codeflow/working-in-codeflow-ide#submitting-a-pr) or just explore the codebase.

### 200 - Opening a specific branch
To inspect a branch with pr.new, visit it on GitHub and in the browser's address tab, add ```pr.new``` to the beginning of the URL, for example:

[https://pr.new/github.com/stackblitz/docs/tree/BRANCH-NAME](https://pr.new/github.com/stackblitz/docs/tree/main)

Or

[https://pr.new/github.com/vanHeemstraSystems/stackblitz-codeflow/tree/main](https://pr.new/github.com/vanHeemstraSystems/stackblitz-codeflow/tree/main)

You will be redirected to [Codeflow IDE](https://developer.stackblitz.com/codeflow/working-in-codeflow-ide) where you can explore the code, continue the work, or investigate the issue.

### 300 - Reviewing a PR
To review a PR with pr.new, visit the submitted pull request on GitHub and in the browser's address tab, add ```pr.new``` to the beginning of the URL, for example:

[https://pr.new/github.com/stackblitz/docs/pull/33](https://pr.new/github.com/stackblitz/docs/pull/33) 

**NOTE**: At the time of this writing the Pull Request "```33```" was already pulled, hence why you won't see the Pull Request in the IDE. If you go to the left-hand menu and choose "Source Control", what you will see is a button "View Closed PR on GitHub", which when clicked will take you to the pulled request "fixes type #33". 

Or 

[https://pr.new/github.com/vanHeemstraSystems/stackblitz-codeflow/pull/1](https://pr.new/github.com/vanHeemstraSystems/stackblitz-codeflow/pull/1)

You will be redirected to [Codeflow IDE](https://developer.stackblitz.com/codeflow/working-in-codeflow-ide) in the "[PR review mode](https://developer.stackblitz.com/codeflow/working-in-codeflow-ide#reviewing-a-pr-with-codeflow-ide)" where you will see diffs. You can switch to the standard file view by choosing the "file" icon in the left vertical nav bar.

## 300 - "Open in Codeflow" button

To help your users quickly spin up the entire environment with your project, you can add a CTA (call-to-action) button on your website or in the README file with any of the above pr.new links.

**TIP**: You can either host the images on your servers or directly use our image URLs.

In order to display the button in a **Markdown file**, use the following code - remember to update the last URL with the project repository path:

```
[![Open in Codeflow](https://developer.stackblitz.com/img/open_in_codeflow_small.svg)](https:///pr.new/___GH_ACCOUNT__/___GH_REPOSITORY___)
```

Replace ```___GH_ACCOUNT__``` with the GitHub Account of the repository you like to link to, replace ```___GH_REPOSITORY___``` with the GitHub Account's Repository you like to link to. 

For example: 

```
[![Open in Codeflow](https://developer.stackblitz.com/img/open_in_codeflow_small.svg)](https:///pr.new/vanHeemstraSystems/stackblitz-codeflow)
```

Or, in HTML:

```
<a href="https:///pr.new/___GH_ACCOUNT__/___GH_REPOSITORY___">
  <img
    alt="Open in Codeflow"
    src="https://developer.stackblitz.com/img/open_in_codeflow_small.svg"
  />
</a>
```

If the user is logged in at GitHub and StackBlitz (in beta), Codeflow IDE will open up. No further configuration is needed.

## 400 - Opening a single file

To edit a single file with pr.new, visit it in the GitHub repository and click the "Edit" icon (a pencil). Now, in the browser's address tab, add ```pr.new``` to the beginning of the URL, for example:

[https://pr.new/github.com/stackblitz/docs/edit/main/docs/guides/user-guide/what-is-stackblitz.md](https://pr.new/github.com/stackblitz/docs/edit/main/docs/guides/user-guide/what-is-stackblitz.md)

You will be redirected to [Web Publisher](https://developer.stackblitz.com/codeflow/content-updates-with-web-publisher) for a more pleasant editing experience. If you prefer to work in a full environment, click on the "Open in IDE" button and you will be redirected to [Codeflow IDE](https://developer.stackblitz.com/codeflow/working-in-codeflow-ide).
