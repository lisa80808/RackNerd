# 支持直连本地模型！免费 AI 代码助手插件：Continue 使用指南

最近我体验了 Cursor 这款 AI 编程工具，特别是它的 Cursor Tab 和 @Codebase 功能让我印象深刻，目前我已经付费使用。不过，我也听到一些开发者的反馈，认为 Cursor 的 20 美元/月的订阅费用有些高昂，希望能找到更经济的替代品。

于是，我向这些开发者推荐了一些国内的 AI 代码补全插件，这些插件大多免费或提供免费试用，可以满足大多数开发需求。然而，有朋友提出了一个更有挑战性的问题：“有没有开源的解决方案？”

经过一番搜索，我发现了一款开源插件：**Continue**。👉 [WildCard | 一分钟注册，轻松订阅海外线上服务](https://bbtdd.com/WildCard)

## 什么是 Continue？

Continue 是一款适用于 **VSCode** 和 **JetBrains** 的插件。它本身不提供 AI 模型，但支持多种接入 AI 模型的方式，能够实现多种场景下的功能。

![Continue 界面](https://bbtdd.com/img/306869352626.webp)

相比直接使用商业插件，开源插件搭配商业模型的方式更加灵活，真正做到“用多少花多少”。更重要的是，**Continue 还支持直连本地模型**，如果你的硬件性能足够强大，完全可以在本地运行一个小型模型来实现 AI 补全。

![自动补全演示](https://bbtdd.com/img/173396130937.webp)

## 安装与配置

### 安装插件

安装 Continue 插件非常简单，只需在 VS Code 的扩展市场中搜索并安装即可。

### 插件配置

插件的配置稍微复杂一些，因为不同的 AI 模型在不同场景下的表现各异。Continue 根据用途将模型分为以下几类：

1. **Tab 补全模型**：适合快速响应，推荐使用 3B 大小的模型。
2. **Chat 模型**：适合对话场景，推荐使用 GPT-4 或 Claude 3.5 Sonnet。
3. **Embeddings 模型**：默认使用本地运行的 Transformers.js，无需额外配置。
4. **Reranking 模型**：主要用于优化代码片段检索，推荐使用 Voyage AI 的 rerank-1。

![模型分类说明](https://bbtdd.com/img/1932753187.webp)

### 在线模型推荐

在在线模型中，我特别推荐 **DeepSeek**，它支持 Chat 和 AutoComplete 功能，且价格相对较低，非常适合个人开发者。

你可以在 [DeepSeek 官网](https://www.deepseek.com) 注册账号并获取 API Key。然后在 Continue 中按照 [DeepSeek 配置文件](https://docs.continue.dev/customize/model-providers/deepseek) 进行配置。

![配置入口](https://bbtdd.com/img/89880465982.webp)

以下是一个基本的配置示例：

json
{
  "tabAutocompleteModel": {
    "title": "DeepSeek Coder",
    "provider": "deepseek",
    "model": "deepseek-coder",
    "apiKey": "[API_KEY]"
  }
}


### 本地模型配置

对于本地模型配置，我推荐使用 **StarCoder2-3B** 模型，它的速度较快且效果不错。你可以在 [Hugging Face](https://huggingface.co/TheBloke/deepseek-coder-6.7B-instruct-GGUF/tree/main) 下载模型文件。

配置完成后，你可以通过本地跑模型实现代码补全，完全无需支付任何费用。

## 体验与总结

实际使用中，Continue 的表现相当不错，特别是在本地模型的支持下，代码补全速度几乎与云端解决方案无异。虽然在某些功能上与商业插件相比略有差距，但 Continue 的灵活性和本地化处理能力使其成为一款非常适合开发者使用的工具。

如果你对隐私和安全性有较高要求，并且希望通过本地 AI 模型提升开发效率，那么 **Continue** 无疑是一个值得尝试的选择。


👉 [WildCard | 一分钟注册，轻松订阅海外线上服务](https://bbtdd.com/WildCard)