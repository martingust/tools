tools
=====

Tools and utility functions used to build and develop Aurelia's libraries.

## To create a dev environment:

1. Create an aurelia directory to hold all of the projects.

  ```shell
  mkdir aurelia
  ```
2. Change to the new directory

  ```shell
  cd aurelia
  ```
3. Clone this repository into the `tools` directory.  This repo contains the helper tools for creating the dev environment.

  ```shell
  git clone https://github.com/aurelia/tools.git
  ```
4. Clone the skeleton-navigation also which is the base app for testing -

  ```shell
  git clone https://github.com/aurelia/skeleton-navigation.git
  ```
5. Change directory into skeleton-navigation

  ```shell
  cd skeleton-navigation
 ```
6. Install the skeleton-navigation application's dependencies:

  ```shell
  npm install
  jspm install
  ```
7. Build the dev environment.  This will create all of the directories inside of `aurelia` under the proper name, `git clone` them all and then perform a `gulp build`.

  ```shell
  gulp build-dev-env
  ```

Now you have the ability to update the repos locally, make changes, and use those in the skeleton app in the `aurelia` directory by using the `gulp update-own-deps` command.

## Aurelia Context Chrome extension instructions

The Aurelia Context Chrome extension is a Chrome extension that lives in the side bar of the elements tab that highlights the current context of the selected element in the DOM.  It works by looking for the view model / context that is currently providing data-binding to the node.  It is in an early beta state and therefore needs to be installed manually instead of through the Chrome Web Store until it is ready for full release.

*Please feel free to open issues in the aurelia/tools repo with possible issues and / or contribute to it's development after signing the CLA*

**Installation**

1. Open your Chrome browser and enter `chrome://extensions` into the URL bar

2. Check the `Developer mode` box to allow adding extensions that aren't from Chrome store

3. Click 'Load Unpacked Extension'

4. Goto the `aurelia/tools/context-debugger` folder and open it

5. The extension should be loaded into your browser.

Right-click on an element and choose `Inspect Element` which should open the Chrome debugging tools.  On the right side pane you should now see an option for `Aurelia Properties` that shows what is currently available.
