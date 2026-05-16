# Day 40 – First GitHub Actions Workflow

## Objective
Learn basic CI/CD using GitHub Actions.
`

<img width="1279" height="611" alt="image" src="https://github.com/user-attachments/assets/1831e8d3-0a6c-4e75-9937-ac4bb3272658" />

`
## Workflow YAML
```bash
name: My First GitHub Actions Workflow

on:
  push:

jobs:
  greet:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout Repository
        uses: actions/checkout@v4

      - name: Print Hello Message
        run: echo "Hello from GitHub Actions!"
        
      - name: Print Date and Time
        run: date

      - name: Print Branch Name
        run: |
          echo "Branch Name: ${{ github.ref_name }}"

      - name: List Repository Files
        run: ls -la

      - name: Print Runner OS
        run: |
          echo "Runner OS: $RUNNER_OS"
        
```
