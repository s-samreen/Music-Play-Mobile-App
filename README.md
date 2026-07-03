# Music Android App

[cite_start]A native Android application project named "Music"[cite: 78]. This repository contains the core build configuration, modules, and multi-platform Gradle wrappers required to setup and run the application.

## Project Structure & Config

[cite_start]The project uses Gradle Kotlin DSL [cite: 2, 3, 77] and is pre-configured with the following settings:

* [cite_start]**AndroidX & Jetifier:** Enabled for modern dependency support and backwards compatibility.
* [cite_start]**Build Optimization:** Uses non-transitive R classes to optimize compilation and reduce build sizes.
* [cite_start]**Memory Tuning:** Configured with `-Xmx2048m` heap size and `UTF-8` encoding for stable daemon performance.
* [cite_start]**Module Inclusions:** Includes the main `:app` module listed in the settings[cite: 78].

### File Overview
* [cite_start]`build.gradle.kts` / `settings.gradle.kts` - Global plugin management and repository resolution (Google, MavenCentral)[cite: 3, 77, 78].
* [cite_start]`gradle.properties` - Build flags and JVM arguments.
* [cite_start]`.gitignore` - Excludes local build directories (`/build`), IDE caches (`.idea`), and user-specific configurations[cite: 1].
* [cite_start]`gradlew` / `gradlew.bat` - Native scripts to run builds without a local Gradle installation.

---

## Local Setup

### 1. Prerequisites
* [cite_start]JDK 17 or higher (Make sure `JAVA_HOME` is set in your env variables)[cite: 35].
* Android SDK setup locally.

### 2. Configure SDK Path
[cite_start]Since `local.properties` is ignored by Git[cite: 1], you need to create this file manually in the root directory and add your local Android SDK path:

```properties
sdk.dir=C\:\\Users\\YOUR_USERNAME\\AppData\\Local\\Android\\Sdk
Build & Run
Open your terminal in the root directory and run the wrapper script:

Windows (CMD / PowerShell):
gradlew.bat build
macOS / Linux:
chmod +x gradlew
./gradlew build
