# ECY AI 插件库

这里存放 ECY 内部使用的 AI 工作流插件。

目前包含 **ECY Review**：用于在邮件、报告、表格、PPT、说明书、图片或 Agent 任务交付前，检查其中的事实、数据、遗漏和实际可用性。

它会先列出问题，不会在检查过程中直接改写原内容。

## 第一次安装

安装前需要满足两点：

- 你的 GitHub 账号已有这个私有仓库的读取权限；
- 你已经在 ChatGPT 或 Codex 中连接 GitHub。

然后新开一个会话，发送：

```text
请从 https://github.com/urspuc/ecy-ai-plugins 导入 ECY 内部插件库，并安装 ECY Review。
```

安装完成后，再新开一个会话使用。

如果你使用 Codex CLI，也可以运行：

```bash
codex plugin marketplace add https://github.com/urspuc/ecy-ai-plugins
codex plugin add ecy-review@ecy-internal
```

## 怎么使用

上传或粘贴需要检查的产物，然后调用 `$ecy-review`。如果有原始需求、规格表或参考资料，最好一起提供。

例如：

```text
$ecy-review 检查这封邮件是否可以发出，重点看有没有未经授权的承诺。
```

```text
$ecy-review 对照附件中的产品规格，检查这份说明书。
```

```text
$ecy-review 检查这个 Excel 的数字和结论是否一致。
```

```text
$ecy-review 判断 Agent 是否真的完成了任务。
```

ECY Review 会自动判断产物类型和检查深度。默认只显示发现的问题、无法验证的内容，以及最值得人工确认的事项。

如果希望它修改内容，请在看完检查结果后再单独说：

```text
请根据已经确认的问题进行修改。
```

## 可以检查什么

- 市场和竞品调研
- Amazon、独立站和商品页面
- 产品规格、说明书和 FAQ
- 商务邮件与对外沟通
- 营销、社媒和品牌文案
- 翻译和本地化
- 表格和数据分析
- PPT、文档和报告
- 图片和视觉设计
- 代码、自动化和 AI Agent 交付
- 销售、渠道和商业分析

## 更新

插件库更新后，重新同步或安装一次，并新开会话，即可使用最新版。
