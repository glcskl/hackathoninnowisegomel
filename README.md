# hackathoninnowisegomel — learning gamification app

An Android application that adds gamification to the learning process: progress is tracked, milestones produce rewards, and streaks encourage daily use. Built for the innowise hackathon on 29 November 2024.

The application lives in the `innowise/` directory. The root of the repository only carries this file.

## Features

- Gamified progress tracking through the learning process
- Reward and milestone system
- Streaks and activity history
- Multiple screens, built as standard Android activities
- XML layouts with Material Design components
- JSON serialisation for storing progress data

## Tech stack

| Layer | Technology |
| --- | --- |
| Platform | Android |
| Language | Java, with Kotlin support in the build |
| Architecture | Activities with XML layouts |
| Serialisation | Gson 2.8.9 |
| Build tooling | Gradle |
| Package | `ry.tech.speedban` |

## Getting started

### Requirements

- Android Studio, with the Android SDK installed
- JDK 8 or newer
- A device or emulator running Android 8.0 or later

### Environment variables

None. The application does not require build-time configuration.

### Installation

```bash
git clone https://github.com/glcskl/hackathoninnowisegomel.git
cd hackathoninnowisegomel/innowise
```

Open the directory in Android Studio and let it resolve the Gradle dependencies, or build from the command line:

```bash
./gradlew assembleDebug
```

The debug APK is written to `app/build/outputs/apk/debug/`.

### Running

Start an emulator or connect a device with USB debugging enabled, then run:

```bash
./gradlew installDebug
```

Open the application from the launcher, or launch it directly:

```bash
adb shell am start -n ry.tech.speedban/.MainActivity
```

## Project structure

```
innowise/
  app/
    build.gradle     application module
    src/main/
      java/ry/tech/speedban/   application code
      res/layout/              XML layouts
      res/menu/                menu resources
      res/mipmap/               launcher icons
  build.gradle       root build configuration
  settings.gradle    module list
  gradle.properties  Gradle settings
```

## SDK versions

| Setting | Value |
| --- | --- |
| `compileSdk` | 35 |
| `targetSdk` | 35 |
| `minSdk` | 27 |
| Source and target compatibility | Java 8 |

## Notes

This is a hackathon project produced under a fixed deadline. Progress is stored on the device and is not synchronised between installations.