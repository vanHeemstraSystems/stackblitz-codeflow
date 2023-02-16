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





MORE ...
