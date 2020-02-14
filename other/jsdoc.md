[Return to Other Professional Works](overview.html)

---

# JSDoc and GitHub Pages

For our JavaScript APIs, we use JSDoc to document our code, and GitHub Pages to host our documentation. Like our main documentation system, GitHub is used to store our API docs.

JSDoc is a markup language used to annotate JavaScript source code files. Using comments containing JSDoc, programmers can add documentation describing the API of the code they're creating. JSDoc then scans the API source code and generates an HTML documentation website.

GitHub Pages is a static site hosting service designed to host HTML pages directly from a GitHub repository. We use GitHub Pages to host our API docs for public consumption at https://apidocs.mycompany.com


## Set Up Your Machine to Generate API Docs

1. Install [node.js](https://nodejs.org/en).
2. Install JSDoc via npm on your local computer: `npm install jsdoc -g`

Fork the following repositories, then clone them to your computer from your GitHub account:

* (Placeholder for code repository)
* (Placeholder for HTML repository for API docs)

## Generate HTML for the API Docs

To generate html documentation for the JavaScript API:

1. Get latest from `code-repository:master`
2. Change directory to the jsdoc folder: `cd %Repository Path%/tools/jsdoc`
3. Run `jsdoc root.js -r api-mainpage.md -c config.json`

This will create all of the HTML files in the `%Repository Path%/tools/jsdoc/out` directory.

## Deploy API Docs

1. Get latest from `html-repository:master`
2. Copy your output from `%Repository Path%/tools/jsdoc/out into `%Repository Path%/html-respository`
3. Push `%Repository Path%/html-repository` to origin and create PR to the upstream.
4. Merge the PR and watch the magic happen.

GitHub Pages will automatically read in the new files and update the live version of the docs on the website.
