Ionic project with CCA structure (Cordova Chrome App)

## First steps

1. clone this repo `git clone git@github.com:felquis/ionic-cca.git && cd ionic-cca`

1. Install cca version 0.5.0 `npm install cca@0.5.0`
  > :warning: You must use CCA 0.5.0 to run this project

1. Ruin `cca upgrade`
  If you see this question:
  > Warning: Upgrade will replace all files in platforms and plugins. Continue? [y/N]
  Answer Y and continue

1. Install these plugins

  ```shell
    cca plugin add org.apache.cordova.device && cca plugin add org.apache.cordova.console && cca plugin add com.ionic.keyboard
  ```

1. Plug your Android device and run `cca run android --device` or `cca emulate ios`

Please, any error trying to startup this repo, [file a issue](https://github.com/felquis/ionic-cca/issues).

Thanks!
