# moodle-project
This is a project template for installing Moodle as a git submodule and all add-ons (plugins) as composer dependencies

This means that the Moodle core can also be managed as a git submodule, and all add-ons (plugins) can be managed with a single `composer.json` file located in the project root.

## Getting started with a new Moodle site
Prerequisites are command line access to Git and Composer.

Change the `your_project` in the following commands to the name of your project.
1. Clone the template from git `git clone https://github.com/fedorsimakov/moodle-project your_project`
2. Go to the cloned directory `cd your_project`
3. Make a new project specific git branch `git checkout -b your_project`
4. Set the desired branch to install Moodle in the `.gitmodules` file
5. Install Moodle core with `git submodule init` and `git submodule update --remote`
6. Install [composer/installers](https://packagist.org/packages/composer/installers) package with `composer install`
7. Install the required plugins from the repository [https://moodleplugarit.mmg.fi](https://moodleplugarit.mmg.fi) and the local repository (`local-repository`) using the command `composer require <vendor> / <plugin_name>`
8. Commit the changes to git
9. Push the project to a git repository host

The new project can now be duplicated to other environments
