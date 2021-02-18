# moodle-project
This is a project template for installing Moodle as a git submodule and all add-ons (plugins) as composer dependencies

This means that the Moodle core can also be managed as a git submodule, and all add-ons (plugins) can be managed with a single `composer.json` file located in the project root.

## Getting started with a new Moodle site
Prerequisites are command line access to Git and Composer.

Change the `your_project` in the following commands to the name of your project.
1. Clone the template from git `git clone https://github.com/fedorsimakov/moodle-project your_project` (or use the repository as a template for a new repository)
2. Go to the cloned directory `cd your_project`
3. Change url "origin" repository to url of your repository `git remote set-url origin https://github.com/your_username/your_project`
4. Make a new project specific git branch `git checkout -b your_project-branch`
5. Set the desired branch to install Moodle in the `.gitmodules` file
6. Install Moodle core with `git submodule init` and `git submodule update --remote`
7. Install [composer/installers](https://packagist.org/packages/composer/installers) package with `composer install`
8. Install the required plugins from the repository [https://moodleplugarit.mmg.fi](https://moodleplugarit.mmg.fi) and the local repository (`local-repository`) using the command `composer require <vendor>/<plugin_name>`
9. Index all added and modified files `git add .`
10. Commit the changes to git `git commit -m "init your_project"`
11. Push the project to a git repository host `git push -u origin --all`

The new project can now be duplicated to other environments
