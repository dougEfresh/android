# Upspin `android` repository

This repository contains experimental support for Upspin on Android.

See the [master repository](https://github.com/upspin/upspin#readme) for more information.

## Building

To build a new APK:

- Download and install Android Studio:
https://developer.android.com/studio/index.html

- Launch Android Studio (<installation_dir>/bin/studio.sh)

- On the main screen, select Import Project (Eclipse, Gradle, etc)
  - Select this project. You should see an Android Studio icon close to it.

- Install an updated Android SDK from within Android Studio.
  - Tools > Android > SDK Manager

- Build go bindings for Android:
  - cd $GOPATH/src/upspin.io/exp/client/gobind
  - go generate

- Import the .aar created in the step above:
  - File > New > New Module > Import .JAR/.AAR Package
  - Enter the path above, expanding the GOPATH var.
  - It should find gobind.aar.
  - Your project window now should have app and gobind.

- Set gobind as a dependency:
  - File > Project Structure
  - Click on "app".
  - Select the Dependencies tab.
  - Click + on the top right margin.
  - Select gobind.
  - Click Ok.

- Build the project
  - Build > Rebuild project

- Plug a phone in Developer Mode and launch the app:
  - Run > Run (or click on the green "play" icon near menu item Run)

- Follow configuration instructions on the phone.
