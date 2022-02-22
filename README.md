## Requirements

In order to initialize themes from this starter, you must have the [Emulsify CLI](https://github.com/emulsify-ds/emulsify-cli) installed as a global package on your machine.

`npm install -g @emulsify/cli`

## Usage

<details><summary>Prerequisites</summary>

Each environment that needs to pull @yalesites-org packages from GitHub needs to be authenticated using a "Personal Access Token". This only needs to be done once per-environment.

- Go to `https://github.com/settings/tokens/new`
  - In the "Note" field add something like "YaleSites GitHub Packages"
  - Choose an expiration value
  - Check the box for "write:packages" (this will automatically check all of the "repo" boxes as well)
  - Click "Generate token"
- On your local machine, create an environment variable. This process varies depending on the shell and operating system you use. It will be something similar to this though: `export KEY=value`.
  - The `key` for YaleSites projects needs to be `YALESITES_BUILD_TOKEN`
  - The `value` is the token you created above
- Done!

</details>

### Initializing a theme

You can initialize a theme as a direct part of a Drupal site, or as a stand-alone project.

<details><summary>As a standalone theme (not in a Drupal project)</summary>

Move ot the location you want to initialize the theme, then run the initi script below. (Choose your own theme name.)

`emulsify init --starter https://github.com/yalesites-org/starter-drupal.git --checkout main "Theme Name" . --platform drupal`

_NOTE: Since we're not in the context of a web project, we pass the 'drupal' platform as our starter of choice._
</details>

<details><summary>Inside an existing Drupal Site</summary>
Move into a Drupal project and run the init script below. (Choose your own theme name.)

`emulsify init --starter https://github.com/yalesites-org/starter-drupal.git --checkout main "Theme Name"`
</details>

### Installing a system

Once you have initialized a theme, cd into your theme, and install a system (the YaleSites system is used in the example below. Update the checkout version to the [latest available](https://github.com/yalesites-org/component-library-twig/releases))

`emulsify system install --repository https://github.com/yalesites-org/component-library-twig.git --checkout v1.3.0`

This will install all required parts of the system. To see what else is available, run the component list command `emulsify component list`. And to install one of the available components run the component install command, e.g. `emulsify component install pull-quote`
