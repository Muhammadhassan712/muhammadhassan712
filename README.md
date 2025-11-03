## 🤖 Auto Reply Bot Example

Here’s an example GitHub Action that replies **"Hello, how are you doing?"**  
whenever someone comments "hello" on your repository issues.

```yaml
name: Auto Reply Bot

on:
  issue_comment:
    types: [created]

jobs:
  reply:
    runs-on: ubuntu-latest
    steps:
      - name: Say hello back
        uses: peter-evans/create-or-update-comment@v3
        if: contains(github.event.comment.body, 'hello')
        with:
          token: ${{ secrets.GITHUB_TOKEN }}
          issue-number: ${{ github.event.issue.number }}
          body: "Hello, how are you doing?"
