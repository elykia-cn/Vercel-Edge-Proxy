# Vercel-Edge-Proxy


## 项目介绍

`Vercel-Edge-Proxy` 是一款免费的全能代理工具，基于 Vercel 平台构建，支持代理全网的 HTTP 和 HTTPS 接口，包括 OpenAI、Midjourney、GitHub、Google、Telegram 等。它可以稳定地在网络环境不佳的情况下运行，适用于单页面应用、API 接口等代理需求。

无论是 OpenAI 等接口服务，还是 GitHub、Google 的资源，都可以通过该代理在国内无科学上网需求的情况下顺利访问，且稳定的 IP 可以确保长期使用不受影响。

**Vercel** 每月提供 100GB 的免费流量，足以满足大多数用户的使用需求。

## 特点

- 支持 OpenAI、Midjourney、GitHub、Google、Telegram 等常见服务的代理。
- 支持 HTTP 和 HTTPS 接口，单页面应用也可以使用。
- 可在网络环境不佳的情况下使用，且代理 IP 稳定。
- 完全免费（非商业用途）。

## 请您 Star / Please Star

如果您觉得此工具不错，请轻轻点击右上角的 **Star** 按钮以增加项目曝光度，谢谢！软件完全免费（商用除外），我们只希望大家能够为项目提供支持并分享给有需要的人，谢谢！

## 部署

点击以下按钮一键部署：

[![Vercel](https://vercel.com/button)](https://vercel.com/import/project?template=https://github.com/elykia-cn/Vercel-Edge-Proxy)

你也可以通过 Fork 本项目后，在 [Vercel](https://vercel.com/) 网站上创建一个新项目。

## 使用方法

1. **部署**：  
   部署方式有两种：  
   - 一键部署：点击上面的部署按钮。  
   - Fork 本项目，登录 Vercel 后创建新项目进行部署。

2. **绑定域名**（可选）：  
   你可以使用 Vercel 提供的免费子域名，或者绑定你自己的域名。  
   绑定域名时，按照 Vercel 上的教程配置即可。你可以通过申请 [tk免费域名](http://www.dot.tk/) 或者从其他域名注册商处获得免费域名。

3. **访问**：  
   部署完成后，使用以下格式访问接口：  
   `https://你的域名/https/url` 或者 `http://你的域名/http/url`  
   其中，`/https/url` 会映射到 HTTPS 接口，`/http/url` 会映射到 HTTP 接口。

## 示例

### 示例 1

访问 `https://你的域名/https/api.openai.com/v1/chat/completions`  
实际上会代理到 `https://api.openai.com/v1/chat/completions`

在一些开源项目中使用时，通常会有类似的配置：  
```python
api_base = os.environ.get("OPENAI_API_BASE", "https://api.openai.com/v1")
```
你只需要将其改为：  
```python
openai.api_base = "https://你的域名/https/api.openai.com/v1"
```
这样就能通过你的代理访问 OpenAI 接口了。

### 示例 2

访问 `https://你的域名/https/github.com/elykia-cn/Vercel-Edge-Proxy`  
实际会被代理到 `https://github.com/elykia-cn/Vercel-Edge-Proxy`

### 示例 3

访问 `https://你的域名/https/www.google.com/search?q=vercel-api-proxy`  
实际会代理到 `https://www.google.com/search?q=vercel-api-proxy`

## 加速 GitHub 下载

如果你需要加速 GitHub 的资源下载，可以使用以下方式：  
原始链接：`https://objects.githubusercontent.com/github-production-release-asset-2e65be/xxxxxx`  
加速后的链接：`https://你的域名/https/objects.githubusercontent.com/github-production-release-asset-2e65be/xxxxxx`

这将显著提升下载速度，尤其在带宽较小的情况下，下载速度可提升数倍。

## 贡献

欢迎提交 Issues 和 Pull Requests！如果你有任何建议或问题，欢迎提出，我们将尽力改进。

---

感谢你使用 `Vercel-Edge-Proxy`！希望这个工具能够为你带来便利。
