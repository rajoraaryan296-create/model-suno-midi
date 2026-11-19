---
layout: default
title: "模型上架：Suno 灵感模式（MIDI 旋律续写）"
description: "第三方接口聚合站 momoAPIPro（tryallapi.com）在 2026 年 11 月 19 日 的系统公告里写明：Suno 全新灵感模式正式上线，支持上传 MIDI 旋律，以你现有的旋律为基底，由 AI 续写创作全新音乐作品。"
---

# 模型上架：Suno 灵感模式（MIDI 旋律续写）

第三方接口聚合站 momoAPIPro（[tryallapi.com](https://tryallapi.com/)）在 **2026 年 11 月 19 日** 的系统公告里写明：Suno 全新灵感模式正式上线，支持上传 MIDI 旋律，以你现有的旋律为基底，由 AI 续写创作全新音乐作品。

要在自己的项目或脚本里按次调用，可以从这个注册入口进入：[https://tryallapi.com/register?aff=5A6A](https://tryallapi.com/register?aff=5A6A)。

本文按 **2026 年 11 月 19 日（Asia/Shanghai，UTC+8）** 对站点系统公告和模型广场截图的复核来写。需要先说清楚：tryallapi.com / momoAPIPro 是**第三方 API 聚合站**，不是 Suno 官网（suno.com），也不是官方 API。模型是否在线、分组是否开放、以及按次价格都会变，请以当天控制台和模型广场为准。同一模型名称也不等于官方直连。

站点模型说明里有这样一句：该 API「用于构建一个与官方Suno网站等效的平台，支持所有官方站点操作」。这是站点自己的表述，并不等于 tryallapi 就是官方 Suno，也不能把它理解成官方服务等级承诺。

## 这个模型是什么

先把三件事分开，避免被中文名「灵感模式」带偏。

### 官方 Create 里的 MIDI 上传

根据 Suno 官方博客 [MIDI in Create](https://suno.com/blog/MIDI-in-create)（Team Suno，2026 年 11 月 4 日）和帮助文档 [Using MIDI files in Create](https://help.suno.com/en/articles/14594177)（2026 年 11 月 4 日修订）：

- MIDI 文件保存的是精确的音符和时值，里面没有音频。
- 可以在 Create 里把 `.mid` / `.midi` 拖进去，或从「+」菜单选择 MIDI，用它作为一首歌的起点。
- 你可以要求 Suno 原样演奏这些音符，也可以只拿一段动机去发展，或换成新的乐器重奏。
- 这和把上传的 WAV / MP3 做 Remix 或 Cover 不同，因为 MIDI 传递的是音符和时值数据。
- 上传方式在 Simple Mode 里，和上传音频、图片一样。官方写明：这项能力在桌面网页端可用，并且面向 Pro、Premier 套餐。
- 步骤是：打开 Create；在 Simple 模式上传或拖入 `.mid` / `.midi`；写一段提示，说明类型、配器、情绪和能量；再点 Create。官方的说法是："Your MIDI shapes the bones of the song. Your prompt shapes everything else."
- 官方还提示：在提示里点名乐器（文件决定演奏什么，提示决定用什么乐器来演奏）；多写感觉，而不只是类型名；Studio 里还可以编辑 MIDI，例如量化（quantize）、人性化（humanize），以及调性和音阶。
- 官方举例可以转述为：写成全编制管弦乐编曲、带钢琴的福音合唱，或弦乐四重奏，并要求严格按照 MIDI 里出现的音符和和弦进行来演奏。本文不另编官方原话。

以上是 suno.com 官方站点的说明。官方写到的 Pro / Premier、桌面网页和 Simple Mode，约束的是官网本身。不要把这些套餐限制直接套到 tryallapi 的调用方头上，也不要假设第三方通道已经取消了这些限制。官网和第三方 API 是两回事。本文也不列举官方套餐价格、积分消耗，或未在上述页面出现的模型名。

### 官方 Inspire 不是上传 MIDI

Suno 帮助中心另有一篇 [Inspire](https://help.suno.com/en/articles/6882753)（2025 年 7 月 21 日修订）。官方这个 Inspire 会根据**你自己做过、并加为 Inspo 的歌单**，再生成一首风格相近的新曲子。入口是 Create 的 Custom Mode 里的 +Inspo 按钮，或歌单顶部的 Inspire 按钮。这是歌单风格参考，**不是**上传 MIDI 旋律，也不是用 MIDI 做续写。

如果把站点公告里的「灵感模式」直接理解成官方这个 Inspire，就容易弄混。下面回到 momoAPIPro 的公告和模型广场，只按截图上的文字来写，也不把站点的「灵感模式」说成官方 Inspire 的同一项功能。

## 渠道：tryallapi.com（momoAPIPro）按量 API

- **站点：** [https://tryallapi.com/](https://tryallapi.com/)
- **注册入口：** [https://tryallapi.com/register?aff=5A6A](https://tryallapi.com/register?aff=5A6A)

这一条面向要在自己的项目、脚本或客户端里调用接口的人，不是 Suno 官方网页。站点品牌是 **momoAPIPro**，定位是按量计费的 API 聚合。这里的 Suno 相关条目是**按次计费**，不是按 token。

2026 年 11 月 19 日，站点系统公告发出：「通知：Suno 全新灵感模式正式上线！支持上传 MIDI 旋律，以你现有的旋律为基底，由 AI 续写创作全新音乐作品。」截图里这条公告显示为「1小时前」。页面没有更精确的钟点，本文也不补写。

![momoAPIPro 系统公告：Suno 全新灵感模式正式上线](https://upload.maynor1024.live/file/1795077245831_01-suno-announcement.png)

> 图注：2026-11-19 系统公告截图。最新一条是「Suno 全新灵感模式正式上线」，截图显示为「1小时前」。同一公告板里也能看到部分模型或分组因资源紧张暂时下架（例如 gemini-4-carbon anti、AWS-Gpt-1），可见上架并不等于所有分组都一直可用。

同一天在模型广场搜索 “suno”，可以看到两条模型，厂商标注都是 Suno，类型都是音视频，标签都能看到「音乐」「按次计费」，并且都可以点「立即体验」：

- `suno_music_open`：卡片上的说明是「Suno API用于构建一个与官方Suno网站等效的平台，支持所有官方站点操作。该模型用于歌曲生成，灵感模式和歌曲续写…」。卡片上的「模型价格」是 $0.0388。打开详情后，标签是「音乐」「异步」；API 端点是 `POST /suno/submit/music`，页面标注为「Suno music generation」。详情里的基本信息写得更完整一些：该模型用于歌曲生成，支持自定义模式、灵感模式和歌曲续写。
- `suno_uploads`：卡片上的「模型价格」是 $0.00162，标签同样是「音乐」「按次计费」。卡片说明几乎被截成只剩下「Suno」，详细功能列表没有出现在这张截图里，本文不补写它具体做什么，也不把它说成 MIDI 上传、音频上传，或另列一张按功能的价目。

左侧筛选项当时显示的是：供应商 Suno 2；全部类型里音视频 2；标签里异步 2、音乐 2；可用专属分组是 Suno-1 x0.1616、Suno-2 x0.2427；计费类型按次计费 2。倍数按页面原样抄录，本文不解释它们如何换算到下面的美元单价表。

![momoAPIPro 模型广场：搜索 suno，以及 suno_music_open 的分组价格](https://upload.maynor1024.live/file/1795077245569_02-suno-models-pricing.png)

> 图注：2026-11-19 模型广场截图。左侧是搜索 “suno” 得到的 `suno_music_open`、`suno_uploads` 两张卡片；右侧是 `suno_music_open` 的详情和分组价格。Suno-2 的价目在截图底部被截断，只露出「发起创作」和「发起创作（Max Mode）」两行。

### 分组价格（2026-11-19 模型广场截图）

计费类型是**按次计费**，单位是每次调用的美元单价，**不是** USD / 1M tokens。下表只抄录截图里能完整看到的数字，使用前请回到控制台和模型广场核对。

**suno_music_open / Suno-1**（按次计费，页面选项为「价格从低到高」）

| 功能 | 价格 |
| --- | --- |
| 发起创作 | $0.1941 |
| 发起创作（Max Mode） | $0.3882 |
| 生成音效 | $0.0388 |
| 人声伴奏分离 | $0.1941 |
| 全轨道混音分离+MIDI | $0.9706 |
| 获取歌词时间线(URL) | $0.0971 |
| 生成歌词 | $0.0000 |
| 提升音乐风格 | $0.0000 |
| 上传参考音频 | $0.0000 |
| 创建歌手风格(Persona) | $0.0000 |

卡片上的「模型价格」$0.0388，和表里「生成音效」这一行的单价一致。详情表是按功能分别标价的，不要把卡片上的这一个数字当成所有功能的统一价。

**suno_music_open / Suno-2**（截图只露出两行）

| 功能 | 价格 |
| --- | --- |
| 发起创作 | $0.2912 |
| 发起创作（Max Mode） | $0.5824 |

Suno-2 其余功能的价格在截图里被截断了，本文不补写。请到当天的模型广场查看完整表格。

`suno_uploads` 的按功能价目没有出现在这张截图里，这里也不编。价格会变，请以控制台和模型广场当天展示为准。本文不引用、不估算官方 Suno API 的价格。

## 怎么接入

1. 打开 [https://tryallapi.com/register?aff=5A6A](https://tryallapi.com/register?aff=5A6A) 注册并登录。
2. 在控制台创建令牌（API Key）。不要把密钥发到聊天、截图或文章里。
3. 接入方式以控制台和当日文档为准。截图里 `suno_music_open` 标明的 API 端点是 `POST /suno/submit/music`（页面标注为「Suno music generation」）。本文不补写未见的完整请求体、鉴权头，也不猜测一条专门给 Suno 用的 Base URL。站点其他模型的 OpenAI 兼容示例里，常见写法是 `https://tryallapi.com/v1`，文档有时也会出现 `https://api.maynorai.asia/v1`；那是针对兼容接点的观察，不能直接当成这条 Suno 端点的完整地址。
4. 实际扣费以控制台账单、当时命中的分组，以及该次调用对应的功能单价为准。

## 需要记住的几点

- 这是第三方按次通道，不是 Suno 官方网站或官方订阅，也不能替代官方账号。
- 站点把自己的 API 写成「与官方Suno网站等效」，这只是站点自己的表述，不等于官方直连，也不等于官方服务等级承诺。
- 站点公告里的「灵感模式」说的是上传 MIDI 旋律、由 AI 续写；官方帮助文档里的 Inspire 说的是按你自己的歌单做风格参考。这两件事不要当成同一个功能。
- 官方 MIDI 上传的套餐和端限制（Pro / Premier、桌面网页、Simple Mode）针对的是 suno.com，不能自动套到 tryallapi 的调用方，也不能理解成站点已经取消了这些限制。
- 上表价格来自 2026 年 11 月 19 日的模型广场截图，按次计费；Suno-2 的价目不完整。价格、分组和可用性都会变，请以当天页面为准。
