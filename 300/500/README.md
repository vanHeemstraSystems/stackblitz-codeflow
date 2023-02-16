# 500 - Integrating Web Publisher

## 100 - What is Web Publisher?
Web Publisher is a page editing tool that makes docs contribution stress-free, including those of us who are not technical.

Web Publisher features a **preview that live updates** as you introduce your edits. **Once you are ready, Web Publisher commits changes, creates a fork and a pull request for you**. You don't need to have the local environment set up, clone the repository, install dependencies, or run the server to see the changes. All this is happening inside your browser.

All you need to edit the docs in Web Publisher is a StackBlitz account.

## 200 - Modifying multiple files
Web Publisher allows you to edit a single page.

However, some edits require modifying a few files. In this case, you can switch to the Codeflow IDE environment, which will run the whole repository.

To do so, click on the "..." icon in the top right corner of the Editor panel, which will show a popup with "Open in Codeflow IDE" button:

You will be redirected to the Web Studio editor and you can continue your work.

## 300 - Adding Web Publisher to your docs
This section will guide you step by step through integrating Web Publisher to your docs.

### 1. Repo compatibility check
Before you begin, verify your toolchain works in WebContainers. To do this, add ```pr.new``` to the beginning of your docs repository GitHub URL.

Example

This is the GitHub address of the StackBlitz docs repo:

[https://github.com/stackblitz/docs/](https://github.com/stackblitz/docs/)

To check if this repo runs in WebContainers, we'll add ```pr.new``` to the beginning of the URL:

[https://pr.new/github.com/stackblitz/docs/](https://pr.new/github.com/stackblitz/docs/)

If you see that **the preview loads correctly**, this means that your dev server runs properly in WebContainers and your repo is compatible.

### 2. Specify the Web Publisher editing link
Let's compose a URL that will specify which file the Web Publisher should feature in the editor and which path to render in the preview. You can use the link generator below or build the link yourself.

Web Publisher links follow this pattern:

https://pr.new/github.com/{repo-owner's-username}/{repo}/edit/{branch}/{file-path-in-the-repo}

For example, here is a Web Publisher link to our docs page:

[https://pr.new/github.com/stackblitz/docs/edit/main/docs/guides/user-guide/what-is-stackblitz.md](https://pr.new/github.com/stackblitz/docs/edit/main/docs/guides/user-guide/what-is-stackblitz.md)

Or,

[https://pr.new/github.com/vanHeemstraSystenms/stackblitz-codeflow/edit/main/README.md](https://pr.new/github.com/vanHeemstraSystems/stackblitz-codeflow/edit/main/README.md)

### 3. Customize the link
Now that you have the base link, you can further customize user experience with query parameters. 

Now that you have the base link, you can further customize user experience with query parameters.

**INFO**: To specify the first parameter, add ```?``` at the end of the base link. Connect the subsequent ones with ```&```.

```initialPath```
**Default behavior**: the Preview window renders the homepage as not always the file path or file name is the same as the rendered route.
**Argument**: A route to be rendered.
**Example**: ```initialPath=guides/user-guide/what-is-stackblitz```

```view```
**Default behavior**: Web Publisher features the Editor and the Preview.
**Argument**: ```editor``` | ```preview``` | ```default```
**Example**: ```view=editor```

### 4. Optional: Installing CodeflowApp bot
**CodeflowApp** is a friendly bot, which provides a one-click link that spins up the whole environment for pull requests and issues. No more context-switching or branch-checkouts, just a new browser tab with a full IDE and a dev server running.

**TIP**: Installing CodeflowApp ensures every commit to default branch and any pull request branches are pre-cloned for instant bootup times. Your project will run faster on Codeflow.

Follow [this integration guide](https://developer.stackblitz.com/codeflow/integrating-codeflowapp-bot) to integrate CodeflowApp bot into your project.

## 400 - "Edit in Web Publisher" button
To help your users easily find their way to Web Publisher on your site or repo, you can add a CTA (call-to-action) button on your website or in the README file.

```
[![Edit in Web Publisher](https://developer.stackblitz.com/img/edit_in_web_publisher_small.svg)](https://pr.new/github.com/vanHeemstraSystems/stackblitz-codeflow/edit/main/README.md)
```

**TIP**: You can either host the images on your servers or directly use our image URLs.

## 500 - Compatibility Mode
In some cases, you may notice the "Compatibility Mode on" banner.

This mode is enabled when Web Publisher is viewed on Safari. [Safari currently doesn't support WebContainers](https://developer.stackblitz.com/platform/webcontainers/browser-support#safari), which is the technology at the basis of Web Publisher.

That being said, you can still run Web Publisher and submit Pull Requests. In this mode, Web Publisher only renders a Markdown-to-HTML conversion. Your app itself it not being run, so there is no app-specific styling, and if you’re using some kind of components in your Markdown, they won’t be compiled.
