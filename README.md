# 材料刊

材料化学阅读器。在手机上像刷小红书一样读 **JACS / Angew / ACS Nano**。与金融顶刊「五大刊」是两条产品线，互不影响。

当前安装包：**[v1.0.2](https://github.com/linshp7-create/cailiaokan/releases/tag/v1.0.2)**（应用名「材料刊」，包名 `com.lin.cailiaokan`）。打开应用会从本仓库拉取最新目录；有新 APK 时应用内提示更新。

第一版只收这三本。Nature Chemistry、Advanced Materials、Nature / Science 材料精选等以后再加。

---

## 读什么

| 卡片缩写 | 全称 |
| --- | --- |
| **JACS** | Journal of the American Chemical Society |
| **Angew** | Angewandte Chemie International Edition |
| **ACS Nano** | ACS Nano |

目录覆盖 **2026 年已出各期**，以及尚未编入正式刊的 **ASAP / Early View**。正式出刊后，早报里的文章会归到对应那一期，不再出现在早报。

这三本都是高产刊。当前目录大约：JACS 32 期、Angew 35 期、ACS Nano 32 期，另有一千多篇 ASAP。App 启动时拉取精简目录 [data/journal-data.app.json](data/journal-data.app.json)（约 3.5MB，不含摘要）。完整带摘要的 [data/journal-data.json](data/journal-data.json) 约十几 MB，只作存档，安装包不会内嵌。点开摘要再按 DOI 向 Crossref 取正文。工作日早上会核对出版社源；有新文或新一期就写进这两个文件。打开 App 即可拉到，不必重装。

---

## 交付标准（与五大刊相同）

1. **手机上读刊**，不在对话里排队出卡片。
2. **一屏很多张**，双列瀑布流。不是一页一张。
3. **两层阅读**：卡片只负责扫，点进去才看摘要、对话、笔记。
4. **中英分开**：英文标题用文字印在图上（不是生成图片）；下面只出中文译名，有翻译才显示。
5. **刊名用英文缩写**（JACS、Angew、ACS Nano）。
6. **已读要记**：打开一篇即记已读；随机流里已读降权，但不隐藏。
7. **私人数据不出手机**：收藏、想法、浏览记录、API 密钥、对话、译文缓存都在本机。
8. **目录和安装包分开更新**：新文只改 JSON；改界面才发新 APK。

---

## 四个栏

**期刊** 杂志封面 → 选 2026 某一期 → 期内双列卡片。

**早报** 还没进正式刊的 ASAP / Early View。

**随机** 双列推荐流。未读优先，已读少出；三刊交错。离开再进不会整墙重洗。

**我的** 收藏、笔记、已读、浏览记录（今天 / 更早），以及本机翻译 / 对话接口。

点卡片进入第二层：**摘要 | 对话 | 笔记**。封面进摘要，「问」进对话。

---

## 翻译和问答（可选）

在「我的」填写自己的 OpenAI 兼容接口（Base URL、模型、密钥）。密钥只存在手机，**不进本仓库、不进 APK**。不填也能读刊、收藏、做笔记。

---

## 安装

1. 打开 [Releases](https://github.com/linshp7-create/cailiaokan/releases/latest)，下载 `cailiaokan.apk`。
2. 若提示未知来源：系统设置 → 应用 → 特殊应用访问 → 安装未知应用。
3. 这是独立应用，不会覆盖「五大刊」。

当前最新：**1.0.2**。

---

## 仓库里有什么

本仓库是 **内容与发布通道**，不是完整 Android 工程。

```
data/journal-data.app.json  精简目录（标题 / 作者 / DOI / 链接 / 页码，App 启动时拉取）
data/journal-data.json      完整目录（含摘要，存档用，App 不拉这个）
README.md                   本说明
```

安装包在 [Releases](https://github.com/linshp7-create/cailiaokan/releases)。`contentVersion` 比本地新时，App 才换目录。摘要在点开后再取，不写进精简 JSON。

---

## 隐私

| 留在手机 | 不进 GitHub / 不进 APK |
| --- | --- |
| 收藏、已读、浏览记录 | API 密钥 |
| 笔记 / 想法 / 评论 | 对话记录 |
| 标题与摘要译文缓存 | 接口设置 |

本仓库公开的是期刊公开目录（标题、作者、摘要、DOI、链接）。论文版权归各期刊与出版社。本项目只做个人阅读入口，不提供全文 PDF。
