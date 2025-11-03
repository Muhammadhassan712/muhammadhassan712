# 🌐 Welcome to Infinite Ville 👋

💻 **Affordable Web Design, Development & Digital Marketing Solutions**

At **Infinite Ville**, we help businesses grow online with custom websites, SEO, and creative marketing — all at budget-friendly rates.

👉 **Visit us:** [https://infiniteville.com/](https://infiniteville.com/)

---

## 🚀 What We Offer
✅ Custom Web Design  
✅ WordPress & eCommerce Development  
✅ SEO Optimization  
✅ Social Media Marketing  
✅ Graphic Design

---

## 🤖 Auto Reply Bot Example

Here’s a simple example of a GitHub Action that automatically replies  
**"Hello, how are you doing?"** when someone comments "hello" on your repository issues.

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
          body: "Hello, how are you doing? Visit us at https://infiniteville.com/"
