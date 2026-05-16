```bash

link : https://github.com/sumitshimpale/github-actions-practices.git
```
Multi Job Workflow

```bash
name: multi job workflow

on:
  push:

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: build step
        run: echo "building the app"

  test:
    runs-on: ubuntu-latest
    needs: build

    steps:
      - name: test step
        run: echo "Running tests"

  deploy:
    runs-on: ubuntu-latest
    needs: test

    steps:
      - name: deploy step
        run: echo "deploying"
```

Environment Variables Workflow

```bash

name: Environment Variables Workflow

on:
  push:

env:
  APP_NAME: myapp

jobs:
  env-demo:
    runs-on: ubuntu-latest

    env:
      ENVIRONMENT: stagging

    steps:
      - name: Print Variables
        env:
          VERSION: 1.0.0

        run: |
          echo "App Name: $APP_NAME"
          echo "Environment: $ENVIRONMENT"
          echo "Version: $VERSION"

      - name: Print GitHub Context Variables
        run: |
          echo "Commit SHA: ${{ github.sha }}"
          echo "Triggered By: ${{ github.actor }}"
```
Conditionals Workflow
```bash
name: Conditionals Workflow

on:
  push:
  pull_request:

jobs:
  conditional-job:
    runs-on: ubuntu-latest

    if: github.event_name == 'push'

    steps:
      - name: Run Only On Main Branch
        if: github.ref == 'refs/heads/main'
        run: echo "Running on main branch"

      - name: Intentional Failure
        run: exit 1
        continue-on-error: true

      - name: Run After Failure
        if: failure()
        run: echo "Previous step failed"

      - name: Always Runs
        run: |
          echo "Workflow continues because continue-on-error is true"
```

Smart Pipeline Workflow
```bash

name: Smart Pipeline

on:
  push:

jobs:
  lint:
    runs-on: ubuntu-latest

    steps:
      - name: Run Lint
        run: echo "Running lint checks"

  test:
    runs-on: ubuntu-latest

    steps:
      - name: Run Tests
        run: echo "Running tests"

  summary:
    runs-on: ubuntu-latest

    needs:
      - lint
      - test

    steps:
      - name: Print Branch Type
        run: |
          if [[ "${GITHUB_REF}" == "refs/heads/main" ]]; then
            echo "This is a main branch push"
          else
            echo "This is a feature branch push"
          fi

      - name: Print Commit Message
        run: |
          echo "Commit Message: ${{ github.event.commits[0].message }}"
```

        
