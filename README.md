# Clash 规则配置

本仓库保存 subconverter 使用的 Clash 外部配置。

Raw 地址：

`https://raw.githubusercontent.com/z15537006222/clash/main/ai-routing.ini`

分流组：

- `🚀 节点选择`：普通海外流量，可以选择全部订阅节点。
- `♻️ AI`：海外 AI，包括 OpenAI/ChatGPT/Codex、Claude、Gemini、NotebookLM、Copilot、Cursor、Grok、Perplexity、Antigravity 等。可以选择全部订阅节点，独立设置出口。
- `YouTuBe`：YouTube 网页、视频、图片、API、YouTube Music，以及规则源维护的 IPv4/IPv6 网段。可以选择全部订阅节点，独立设置出口。
- `🎵 TikTok`：TikTok 及现有相关服务，保留原节点筛选规则。
- `🎯 国内直连`：中国域名、IP、中国 AI 和原有直连例外，使用 `DIRECT`。
- `🐟 漏网之鱼`：未命中其他规则的流量，保留原有出口选项。

中国 AI 优先直连，包括 DeepSeek、通义/Qwen、豆包、Kimi、智谱、MiniMax、Trae、Coze、Qoder 等；中国厂商国际版中被海外 AI 列表收录的域名也优先排除。

海外 AI 使用 MetaCubeX 的 `category-ai-!cn` 汇总规则，中国 AI 使用 `category-ai-cn`、字节 AI 列表和显式补充规则；YouTube 使用 blackmatrix7 的 `YouTube`、`YouTubeMusic` 规则。均引用 subconverter 可读取的文本规则格式。

规则按先后顺序匹配：中国 AI 直连优先于海外 AI 和 TikTok；海外 AI、YouTube 优先于普通海外及中国 IP 规则。原有手动指定的 AI 组辅助域名继续保留。

规则源会随订阅转换更新。YouTube 与其他 Google 服务共享的动态 IP 主要依靠域名规则识别，未将整个 Google IP 范围归入 YouTuBe。更新配置后，需要在客户端刷新订阅，并使用规则模式。
