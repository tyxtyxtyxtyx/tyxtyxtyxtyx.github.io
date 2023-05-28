
### 1. 功能简介

一个简单的GitHub Action示例，它会在本仓库有新的issue时，自动回复一个预设的内容:

### 2. 操作步骤

1. 首先，在您的GitHub仓库中创建一个新目录，例如“.github/workflows”。
2. 在该目录中创建一个新文件，例如“auto-reply.yml”。
3. 在“auto-reply.yml”文件中添加代码，在第五步下面的代码块中。
4. 保存并提交“auto-reply.yml”文件到GitHub仓库。
5. 当您的仓库有新的issue时，GitHub将自动运行该Action，并在新issue下回复一条内容为“Thank you for your issue! Our team will review it and get back to you shortly.”的评论。

```yaml
name: Auto-reply to new issues

on:
  issues:
    types: [opened]

jobs:
  auto_reply:
    runs-on: ubuntu-latest
    steps:
    - name: Auto-reply to new issues
      uses: cj-mills/auto-reply-workflow@main
      with:
        issue-comment: "Thank you for your issue! Our team will review it and get back to you shortly."
```
