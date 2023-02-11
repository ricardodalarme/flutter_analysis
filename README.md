# Flutter Analysis

[![pub_badge]][pub_badge_link]
[![badge]][badge_link]
[![license_badge]][license_badge_link]


This package provides a set of rules for Dart and Flutter to develop with the best possible practices. For more information, see the [complete list of options][analysis_options_yaml].

## Usage

To use the lints, add as a dev dependency in your `pubspec.yaml`:

```yaml
dev_dependencies:
  flutter_analysis: ^1.0.0
```

Then, add an include in `analysis_options.yaml`:

```yaml
include: package:flutter_analysis/recommended.yaml
```

```

## Suppressing Lints

There may be cases where specific lint rules are undesirable. Lint rules can be suppressed at the line, file, or project level.

An example use case for suppressing lint rules at the file level is suppressing the `prefer_const_constructors` in order to achieve 100% code coverage. This is due to the fact that const constructors are executed before the tests are run, resulting in no coverage collection.

### Line Level

To suppress a specific lint rule for a specific line of code, use an `ignore` comment directly above the line:

```dart
// ignore: public_member_api_docs
class A {}
```

### File Level

To suppress a specific lint rule of a specific file, use an `ignore_for_file` comment at the top of the file:

```dart
// ignore_for_file: public_member_api_docs

class A {}

class B {}
```

### Project Level

To suppress a specific lint rule for an entire project, modify `analysis_options.yaml`:

```yaml
include: package:flutter_analysis/recommended.yaml
linter:
  rules:
    public_member_api_docs: false
```

## Badge

To indicate your project is using `flutter_analysis` →
[![badge]][badge_link]

```md
[![style: flutter_analysis](https://img.shields.io/badge/style-flutter__analysis-purple)](https://pub.dev/packages/flutter_analysis)
```

[analysis_options_yaml]: https://github.com/ricardodalarme/flutter_analysis/blob/main/lib/recommended.yaml
[badge]: https://img.shields.io/badge/style-flutter_analysis-B22C89.svg
[badge_link]: https://pub.dev/packages/flutter_analysis
[license_badge]: https://img.shields.io/badge/license-MIT-blue.svg
[license_badge_link]: https://opensource.org/licenses/MIT
[pub_badge]: https://img.shields.io/pub/v/flutter_analysis.svg
[pub_badge_link]: https://pub.dartlang.org/packages/flutter_analysis
