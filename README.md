Ionic project with CCA structure (Cordova Chrome App)

## First steps

1. clone this repo `git clone git@github.com:felquis/ionic-cca.git && cd ionic-cca`

1. Install cca version 0.5.0 `npm install cca@0.5.0 -g`
  > :warning: You must use CCA 0.5.0 to run this project

  You may need to use `sudo` to install with `-g` flag

1. Run `cca upgrade`
  If you see this question:
  > Warning: Upgrade will replace all files in platforms and plugins. Continue? [y/N]
  Answer Y and continue

1. Install these plugins

  ```shell
    cca plugin add org.apache.cordova.device && cca plugin add org.apache.cordova.console && cca plugin add com.ionic.keyboard
  ```

1. Plug your Android device and run `cca run android --device` or `cca emulate ios`

## Cordova plugins compability notes
Here are described known workarounds for issues related to Cordova's plugin incompabilities with Crosswalk.
### File Transfer Plugin
If you are going to use the [Cordova File Transfer] (https://github.com/apache/cordova-plugin-file-transfer) plugin in your project, you should be awared that this plugin is incompatible with Crosswalk engine that the CCA is built upon.

The reason of application crash is that file transfer plugin uses Android's native ```android.webkit.CookieManager```. Be sure you want to use ```org.xwalk.core.internal.XWalkCookieManager``` instead. More details in this [commit] (https://github.com/gaochun/cordova-plugin-file-transfer/commit/0063249e279b99a0feb4601650fc3a4c9e8a8ed2)

Here is the corrected plugin version for your project: https://github.com/AleksMeshkov/cordova-plugin-file-transfer
You can install it by the following command: ```cca plugin add https://github.com/AleksMeshkov/cordova-plugin-file-transfer```

Please, any error trying to startup this repo, [file a issue](https://github.com/felquis/ionic-cca/issues).

Thanks!
