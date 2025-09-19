name: Update Recent Activity

on:
  schedule:
    - cron: "0 * * * *" # updates every hour
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3

      - name: Recent Activity
        uses: Readme-Workflows/recent-activity@v2
        with:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
