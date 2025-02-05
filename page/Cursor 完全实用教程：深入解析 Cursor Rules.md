# Cursor 完全实用教程：深入解析 Cursor Rules

![Cursor Rules](&thumbnail=660x2147483647&quality=80&type=jpg)

大家好，我是章北海

在之前的文章中，我已经详细介绍了 Cursor 这一神级代码编辑器，并分享了如何通过 Cursor + Claude 完成一个完整的项目开发。自从使用了 Cursor，我已经很久没有使用 ChatGPT 了。

今天，我们将深入探讨 Cursor 中的 `Rules for AI` 和 `.cursorrules` 文件的关系、优先顺序及其具体使用方法。

## Cursor 中的 Rules for AI 与 .cursorrules 文件

![Cursor Settings](&thumbnail=660x2147483647&quality=80&type=jpg)

`Rules for AI` 在 Cursor 的设置中填写后，会在 Cursor Chat 和 Ctrl/⌘ K 时生效，功能类似于 **system prompt**。

### `.cursorrules` 文件的作用

`.cursorrules` 文件用于根据项目的特定需求调整 AI 的响应，确保代码建议更加相关和准确。以下是其主要优点：

- **定制 AI 行为**：通过 `.cursorrules` 文件，可以根据项目需求调整 AI 的响应，确保代码建议更符合项目需求。
- **一致性**：定义编码标准和最佳实践，确保 AI 生成的代码与项目样式保持一致。
- **上下文意识**：提供项目的重要上下文信息，如常用方法、架构决策或特定库，使代码生成更具洞察力。
- **提高生产力**：通过明确的规则，AI 生成的代码需要更少的手动编辑，从而加速开发过程。
- **团队对齐**：在团队项目中，共享 `.cursorrules` 文件可以确保所有团队成员获得一致的 AI 辅助，促进编码实践的一致性。
- **项目特定知识**：包含项目结构、依赖关系或独特需求的信息，帮助 AI 提供更准确和相关的建议。

`.cursorrules` 文件中的规则同样适用于 **Cursor Chat** 和 **Ctrl/K** 等功能。

## 如何使用 `.cursorrules` 文件？

![Cursor Rules Example](&thumbnail=660x2147483647&quality=80&type=jpg)

不同的项目需要支持不同的 `cursor rules`，只需要将 `.cursorrules` 文件添加到项目的根目录下即可。例如，如果你的项目是 **Python 数据可视化**、**机器学习建模** 或 **前端/后端开发**，你只需从相关网站复制对应的 `prompt`，然后在项目根目录中创建 `.cursorrules` 文件并粘贴即可。

![Multi-Project Rules](&thumbnail=660x2147483647&quality=80&type=jpg)

### 优先级问题

根据我的测试，`Rules for AI` 和 `.cursorrules` 文件的优先级如下：

1. `Rules for AI` 优先于 `.cursorrules` 文件生效。
2. 如果在工作空间中打开多个文件夹，第一个文件夹下的 `.cursorrules` 文件会生效。

有人提到：

> 当你在进行项目时，你可能会在工作空间中打开多个仓库。一个用于后端，一个用于前端，每个仓库可能有自己的语言（例如，后端使用 python/fastapi，前端使用 JS/React）。然后你可能需要为每个仓库创建一个单独的 `.cursorrules` 文件，每个文件中的规则适应于每个仓库中的技术栈。

目前来看，似乎无法实现这一点，至少无法同时生效。

👉 [WildCard | 一分钟注册，轻松订阅海外线上服务](https://bbtdd.com/WildCard)