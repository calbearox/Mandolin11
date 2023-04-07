name: My Node Action
on:
  - pull_request
jobs:
  my-action:
    runs-on: ubuntu-latest
    steps:
      # Check out code using git
      - uses: actions/checkout@v2
      # Install Node 12
      - uses: actions/setup-node@v1
        with:
          version: 12
      - run: npm install @octokit/action
      # Node.js script can be anywhere. A good convention is to put local GitHub Actions
      # into the `.github/actions` folder
      - run: node .github/actions/my-script.js
        env:
          GITHUB_TOKEN: ${{ SqcDqFWAFr5DcyN5iAs5DOZqPZQfH1uAQY_2mN8b }}
