## Usage

To initialize a theme, move into a Drupal project and run the init script below. (Choose your own theme name.)

`emulsify init --starter https://github.com/yalesites-org/starter-drupal.git --checkout main "Theme Name"`

Then, cd into your theme, and install a system (the YaleSites system is used in the example below.)

`emulsify system install --repository https://github.com/yalesites-org/component-library-twig.git --checkout v1.2.0`

This will install all required parts of the system. To see what else is available, run the component list command `emulsify component list`. And to install one of the available components run the component install command, e.g. `emulsify component install pull-quote`
