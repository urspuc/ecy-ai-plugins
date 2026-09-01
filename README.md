# ECY AI Plugins

Internal AI workflows for ECY. This marketplace currently contains **ECY Review**, a review-first skill for checking AI-generated work before it is used, sent, published, or treated as complete.

## Install

The shortest path is to connect GitHub, start a new ChatGPT Work or Codex conversation, and send:

```text
请从 https://github.com/urspuc/ecy-ai-plugins 导入 marketplace，并安装 ECY Review。
```

Because this is a private repository, the GitHub account connected by each colleague must already have read access to `urspuc/ecy-ai-plugins`.

### ChatGPT desktop

1. Open **Plugins** and choose **Add Marketplace**.
2. Import this GitHub repository.
3. Start a new conversation, select **ECY Review**, and attach or paste the artifact.

The marketplace marks ECY Review as installed by default. If it does not appear immediately, refresh or restart ChatGPT after the marketplace finishes syncing.

### Codex CLI or IDE

Add the GitHub marketplace:

```bash
codex plugin marketplace add https://github.com/urspuc/ecy-ai-plugins
```

Then start a new conversation. If the host does not install default marketplace entries automatically, install it once:

```bash
codex plugin add ecy-review@ecy-internal
```

## Use

ECY Review is explicit-only. It will not activate merely because a conversation mentions checking or reviewing.

In ChatGPT, select or mention **ECY Review**. In Codex, invoke:

```text
$ecy-review 检查这个产物是否可以交付
```

More examples:

```text
$ecy-review 检查这封邮件，重点看有没有未经授权的承诺
```

```text
$ecy-review 对照附件中的产品规格，深度检查这份说明书
```

```text
$ecy-review 判断 Agent 是否真的完成了任务
```

The skill automatically identifies the artifact type, chooses a risk-appropriate review depth, and loads only the relevant checklist. Its first pass reports problems and verification gaps without rewriting the artifact.

## Included review routes

- Research and competitor analysis
- Ecommerce, Amazon and product listings
- Product specifications, manuals and FAQs
- External email and business communication
- Marketing, social and brand copy
- Translation and localization
- Spreadsheet and data analysis
- Presentations, documents and reports
- Images and visual design
- Coding, automation and agent completion
- Sales, channel and commercial analysis

## Update

Marketplace imports can sync new repository versions. Start a new conversation after an update so the host loads the latest skill instructions.
