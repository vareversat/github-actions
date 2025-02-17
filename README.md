# github-actions 🚀

A curated collection of reusable GitHub Actions workflows organized by programming language and technology stack, plus general-purpose workflows for common development tasks.

## Repository Structure 📁

```
.
├── go/
│   ├── test.yml
│   ├── lint.yml
│   └── ...
├── flutter/
│   ├── test.yml
│   ├── build.yml
│   └── ...
├── general/
│   ├── release.yml
│   ├── deploy.yml
│   └── ...
└── [other-language]/
    └── [command].yml
```

## Naming Convention 📝

All workflow files follow this naming pattern:
```
[language/category]/[command].yml
```

For example:
- `go/test.yml`
- `flutter/test.yml`
- `general/release.yml`

## Usage 💡

To use these workflows in your projects, add a new workflow file in your repository's `.github/workflows` directory with the following structure:

```yml
name: Call a reusable workflow

on:
  workflow_dispatch:
  pull_request:

jobs:
  call-workflow:
    uses: vareversat/github-actions/go/lint.yml@main
    with:
      # Add any required inputs here
      parameter1: value1
      parameter2: value2
```

For more detailed information about reusing workflows, check out the [GitHub documentation on reusable workflows](https://docs.github.com/en/actions/sharing-automations/reusing-workflows#calling-a-reusable-workflow).

## Available Workflows ⚙️

### Go 🔵
- `test.yml`: Run Go tests
- `lint.yml`: Lint Go code

### Flutter 💙
- `test.yml`: Run Flutter tests
- `build.yml`: Build Flutter applications

### General Purpose 🛠️
- `release.yml`: Create project releases
- More general-purpose workflows will be added here

[Other sections will be added as more workflows are included]

## Contributing 🤝

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.
