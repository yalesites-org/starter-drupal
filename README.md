## Requirements

In order to initialize themes from this starter, you must have the [Emulsify CLI](https://github.com/emulsify-ds/emulsify-cli) installed as a global package on your machine.

`npm install -g @emulsify/cli`

## Usage

### As a standalone theme (not in a Drupal project)

Move ot the location you want to initialize the theme, then run the initi script below. (Choose your own theme name.)

`emulsify init --starter https://github.com/yalesites-org/starter-drupal.git --checkout main "Theme Name" . --platform drupal`

_NOTE: Since we're not in the context of a web project, we pass the 'drupal' platform as our starter of choice._

### Inside an existing Drupal Site
Move into a Drupal project and run the init script below. (Choose your own theme name.)

`emulsify init --starter https://github.com/yalesites-org/starter-drupal.git --checkout main "Theme Name"`

### Installing a system

Once you have initialized a theme, cd into your theme, and install a system (the YaleSites system is used in the example below. Update the checkout version to the [latest available](https://github.com/yalesites-org/component-library-twig/releases))

`emulsify system install --repository https://github.com/yalesites-org/component-library-twig.git --checkout v1.3.0`

This will install all required parts of the system. To see what else is available, run the component list command `emulsify component list`. And to install one of the available components run the component install command, e.g. `emulsify component install pull-quote`
