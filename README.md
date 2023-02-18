Step-By-Step Guides to Setting Up Your Device

# MacOS

1. Install [Visual Studio Code](https://code.visualstudio.com/sha/download?build=stable&os=darwin-universal)
1. Install [Python](https://www.python.org/ftp/python/3.11.2/python-3.11.2-macos11.pkg)
   * After you download and go through the install, open the **Terminal** and type `python3 --version`. It should show some numbers on the next line. This confirms that the installation was successful.

# Windows
1. Install [Visual Studio Code](https://code.visualstudio.com/sha/download?build=stable&os=win32-x64-user)
2. Install [Python](https://www.python.org/ftp/python/3.11.2/python-3.11.2-amd64.exe)
   * Open **System Environment Variables** and add to Path the 
   * Open **Command Prompt** (Win+R, search for "cmd.exe") and type `python3 --version`
  
# iGEM TeamName Wiki

This repository **MUST** contain all coding assets to generate your team's wiki (HTML, CSS, JavaScript, TypeScript, Python, etc).

Images, photos, icons and fonts **MUST** be stored on `static.igem.wiki` using [uploads.igem.org](https://uploads.igem.org), and Videos **must** be embedded from [iGEM Video Universe](https://video.igem.org).

For up-to-date requirements, resources, help and guidance, visit [competition.igem.org/deliverables/team-wiki](https://competition.igem.org/deliverables/team-wiki).

## Getting started

You should probably only edit the files inside folders `static`, `wiki` and `wiki > pages`.
1. Open the Web IDE
1. Make the changes on the files you wish:
    * For the menu, change the file [menu.html](wiki/menu.html)
    * For the layout, change the file [layout.html](wiki/layout.html)
    * For the pages, change the corresponding file in the foler [pages](wiki/pages)
1. Review the changes you made
1. Once you are done, save the changes by **committing** them to the *main branch* of the repository
1. An automated script will build, test and deploy your wiki, which should take less than 30 seconds.

## About this Template

### Files

The static assets are in the `static` directory. The layout and templates are in the `wiki` directory, and the pages live in the `wiki > pages` directory. Unless you are an experienced and/or adventurous human, you probably shouldn't change other files.

    |__ static/             -> static assets (CSS and JavaScript files only)
    |__ wiki/               -> Main directory for the pages and layouts
        |__ footer.html     -> Footer that will appear in all the pages
        |__ layout.html     -> Main layout of your wiki. All the pages will follow its structure
        |__ menu.html       -> Menu that will appear in all the pages
        |__ wiki-tools.html -> Wiki tools to help getting started with this template
        |__ pages/          -> Directory for all the pages
            |__ *.html      -> Actual pages of your wiki
    |__ .gitignore          -> Tells GitLab which files/directories should not be uploaded to the repository
    |__ .gitlab-ci.yml      -> Automated flow for building, testing and deploying your website.
    |__ LICENSE             -> License CC-by-4.0, all wikis are required to have this license - DO NOT MODIFY
    |__ README.md           -> File containing the text you are reading right now
    |__ app.py              -> Python code managing your wiki
    |__ dependencies.txt    -> Software dependencies from the Python code

### Technologies

  * [GitLab Pages](https://docs.gitlab.com/ee/user/project/pages/)
  * [Python](https://www.python.org): Programming language
  * [Flask](https://palletsprojects.com/p/flask/): Python framework
  * [Fronzen-Flask](https://pythonhosted.org/Frozen-Flask): Library that builds the wiki to be deployed as a static website
  * [Bootstrap](https://getbootstrap.com/docs/5.0/components): CSS and JS components used

### Building locally (advanced users)

To work locally with this project, you'll have to follow the steps below:

#### Install
```bash
git clone https://gitlab.igem.org/templates/wiki-frozen-flask
cd example
python3 -m venv venv
. venv/bin/activate
pip install -r dependencies.txt
```

#### Execute
```bash
python app.py
```
