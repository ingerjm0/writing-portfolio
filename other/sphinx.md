[Return to Other Professional Works](overview.html)

---

# Sphinx and Read the Docs

For the main documentation system, we use **Sphinx** to generate it, and **Read the Docs** to publish/host it. GitHub is a helpful middleman and stores all of the docs.

**Sphinx** is an open-source, robust solution for software documentation that includes features that writers expect, like:

* Single Source Publishing (HTML, PDF, ePub, and more)
* Content reuse through includes
* Multiple mature HTML themes that provide great user experience on mobile and desktop
* Referencing across pages, documents, and projects
* Index and Glossary support
* Localization support

**Read the Docs** is a hosting platform for Sphinx-generated documentation. It takes the power of Sphinx and adds version control, full-text search, and other useful features. It pulls down code and doc files from Git then builds and hosts the documentation. 

## Install Sphinx for Local Builds

We encourage you to compile the documentation locally on your computer prior to submitting a PR. To install Sphinx: 

1. Run cmd as administrator.
2. Install Chocolatey via the cmd (on one line):

    ```
    @"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"
    ```

3. Install Python 3 via Chocolatey via the cmd:

    ```
    C:\> choco install python
    ```

4. Restart cmd or refresh with the command:

    ```
    C:\> refreshenv
    ```

5. Install Sphinx in a command line:

    ```
    C:\> pip install -U sphinx
    ```

6. Install the Markdown parser recommonmark:

    ```
    C:\> pip install --upgrade recommonmark
    ```

7. Install our Sphinx theme:

    ```
    C:\> pip install sphinx_rtd_theme
    ```
               
### Compile the Documentation Locally

1. Fork and clone the documentation branch from GitHub.
2. Using a command line, cd to your local repository, then the docs folder.
3. Compile with the command `make html`.

The HTML output will be in build\html. Open index.html in a browser to view docs.


## Update the Live Documentation System

Our system is set up so that Read the Docs automatically manages versioning of our help system, and monitors the GitHub repository for changes to the docs.

* The master branch will our "development" branch.
* Branches per release will be called the release - RC79, etc
* If we have to push docs between releases, we will use the last version’s branch.

Therefore, follow these procedures when checking in documentation changes:

**If you're pushing to a future version that hasn't been cut:** 
1. Create a PR to the master branch.

**If you're pushing to a future version that HAS already been cut:**
1. Create two PRs: one to the master branch and another to the release branch

**If you're pushing to a past version:**
1. Create two PRs: one to the master branch and another to the release branch

Once you merge your PR(s), Read the Docs will automatically generate the docs:

1. The master branch will be pushed to https://docs.mycompany.com/en/latest. THIS IS PRIVATE and only viewable by members of the
Organization in Read the Docs.
2. The release branch will be pushed to https://docs.mycompany.com/en/RCxx. These branches are public unless they are not released.

(Note that the visibility of branches is controlled by the organization admin for our company's Read the Docs account)


## Using RST 

Most of our docs use RST. reStructuredText (RST) is the default plaintext markup language used by Sphinx. It is an extensible markup language, that is fully customizable. However, we don't (yet) have need of this, and will stick with the default set of directives for our documentation. To learn more, refer to Sphinx's [reStructuredText Primer](https://www.sphinx-doc.org/en/2.0/usage/restructuredtext/basics.html).
