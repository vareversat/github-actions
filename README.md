# github-actions 🚀

A curated collection of reusable GitHub Actions workflows organized by programming language and technology stack, plus general-purpose workflows for common development tasks.

## Repository Structure 📁

```
.
├── .github/
│   └── workflows/
│       ├── go.test.yml
│       ├── go.lint.yml
│       ├── ...
│       ├── flutter.test.yml
│       ├── flutter.build.yml
│       ├── ...
│       ├── general.release.yml
│       ├── general.deploy.yml
│       ├── ... 
|       ├── [language/category].[command].yml
```

## Naming Convention 📝

All workflow files follow this naming pattern:
```
[language/category].[command].yml
```

For example:
- `go.test.yml`
- `flutter.test.yml`
- `general.release.yml`

## Usage 💡

To use these workflows in your projects, add a new workflow file in your repository's `.github/workflows` directory with the following structure:

```yml
name: Call a reusable workflow

on:
  workflow_dispatch:
  pull_request:

jobs:
  call-workflow:
    uses: vareversat/github-actions/.github/workflows/go.lint.yml@main
    with:
      # Add any required inputs here
      parameter1: value1
      parameter2: value2
```

For more detailed information about reusing workflows, check out the [GitHub documentation on reusable workflows](https://docs.github.com/en/actions/sharing-automations/reusing-workflows#calling-a-reusable-workflow).

## Available Workflows ⚙️

### Docker

- `docker.build-push.yml`: Docker build & push images into Github registry

### Go

- `go.lint.yml`: Lint Go code
- `go.test.yml`: Run Go tests
- `go.list.yml`: List Go dependencies
- `go.build.yml`: Build Go binaries on Mac, Win & Linux OS + upload artifacts

### Fastlane

- `fastlane.lane.yml`: Compute the lane name based on the last push type

### Flutter

- `flutter.analyze.yml`: Run Flutter analyzes
- `flutter.format.yml`: Run Flutter format
- `flutter.test.yml`: Run Flutter tests
- `flutter.build.yml`: Build Flutter applications

### Firebase

- `firebase.function.lint.yml`: Lint Typescript code
- `firebase.function.publish.yml`: Build and deploy functions

### General Purpose

- `global.release.yml`: Create project releases
- `global.page.yml`: Publish Github page

[Other sections will be added as more workflows are included]

## Contributing 🤝

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.
