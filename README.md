Ionic project with CCA structure (Cordova Chrome App)

## First steps

1. clone this repo `git clone git@github.com:felquis/ionic-cca.git && cd ionic-cca`

1. Install cca version 0.4.3 `npm install cca@0.4.3`

1. run `cca platform add android` or ios

1. Install plugins

  ```shell
    cordova plugin add org.apache.cordova.device && cordova plugin add org.apache.cordova.console && cordova plugin add com.ionic.keyboard
  ```
1. run again `cca platform add android` or ios
   PS: If cca log `Platform android already added`, just run `cca platform remove android` and than tun `cca platform add android` again

1. Plug your Android device and run `cca run android --device` or `cca emulate ios`

## Running on iOS/Android

CCA may output `Warning: Upgrade will replace all files in platforms and plugins. Continue? [y/N]`, choosing `N`, anything will happens, choosing `Y` the folder `platforms/` and `plugins` will be deleted.

When these folder be deleted, a file called `created-with-cca-version` will be created, with the version of your current cca (this is annoying)

So, you need to back to the first step of the README, and start again, one time this file `created-with-cca-version` is there, CCA wont ask for it again.

Please, any error trying to startup this repo, [file a issue](https://github.com/felquis/ionic-cca/issues).

Thanks!

