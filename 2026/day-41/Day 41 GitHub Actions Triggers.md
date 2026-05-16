```bash

https://github.com/sumitshimpale/github-actions-practices.git
```

```bash
.github/workflows/
├── hello.yml
├── pr-check.yml
├── manual.yml
├── schedule.yml
└── matrix.yml
```

1.Pull Request Workflow

```bash

name: PR Check Workflow

on:
  pull_request:
    branches:
      - main

jobs:
  pr-check:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout Code
        uses: actions/checkout@v4

      - name: Print PR Branch
        run: |
          echo "PR check running for branch: ${{ github.head_ref }}"

```

2.Scheduled Workflow

```bash

name: Schedule Workflow

on: 
  schedule:
    - cron: '0 0 * * *'

jobs: 
  schedule-job:
    runs-on: ubuntu-latest

    steps:
      - name: Print Schedule Message
        run: echo "Scheduled workflow executed"
```


3.Manual Workflow

```bash

name: manual Workflow

on:
  workflow_dispatch:
    inputs:
      environment: 
        description: "Enter env name"
        required: true
        default: "staging"

jobs:
  manual-job:
    runs-on: ubuntu-latest

    steps:
      - name: Print environment
        run: |
          echo "selected environment: ${{ github.event.inputs.environment }}"

```

4.matrix workflow

```bash

name: matrix workflow

on:
  push:

jobs:
  matrix-job:
    runs-on: ${{ matrix.os }}

    strategy:
      matrix:
        os:
          - ubuntu-latest
          - windows-latest
        
        python-version:
          - "3.10"
          - "3.11"
          - "3.12"

    steps:
      - name: Checkout Code
        uses: actions/checkout@v4

      - name: setup python
        uses: actions/setup-python@v5
        with:
          python-version: ${{ matrix.python-version }}

      - name: Print Python Version
        run: python --version

      - name: Print Operating system
        run: |
          echo "Running on $RUNNER_OS"

```
## What I Learned

- GitHub Actions can trigger on PRs
- Workflows can run on schedules
- Manual workflows accept inputs
- Matrix builds run jobs in parallel
- fail-fast controls matrix behavior

<img width="1279" height="653" alt="image" src="https://github.com/user-attachments/assets/a978ea3e-4af4-4784-8980-182788bfcfea" />

