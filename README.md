# Kotlin Starter Project

A modern Kotlin project template with pre-configured build conventions and automated dependency management.

## Features

### Gradle Convention Plugins

This project leverages Gradle Convention Plugins to maintain consistent build configuration across all modules. The following plugins come pre-configured:

| Plugin     | Purpose                 | What it provides                            |
|------------|-------------------------|---------------------------------------------|
| **Kotlin** | Kotlin language support | Compiler settings, JVM target configuration |
| **Detekt** | Static code analysis    | Code smell detection, quality metrics       |
| **Ktlint** | Code formatting         | Consistent code style enforcement           |
| **Test**   | Testing framework       | JUnit 6 + Kotest assertions setup           |

Apply these plugins to any module by adding them to your `build.gradle.kts`:

```kotlin
plugins {
    id("kotlin-conventions")
    id("test-conventions")
}
```

### Dependency Management

This project uses the [refreshVersions](https://github.com/jmfayard/refreshVersions) Gradle plugin for centralized dependency version management. All dependency versions are stored in `versions.properties`, making it easy to track and update dependencies across all modules.
Dependencies are referenced using the underscore placeholder (`_`) instead of hardcoded versions.
