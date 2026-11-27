# 同人图鉴（Fanwork Atlas）

这是同人图鉴的公开云端词库，为酒馆助手插件提供角色和作品数据。同人图鉴支持在 SillyTavern 与 TT 酒馆中按角色或作品检索，也可以把匹配到的条目同步到「同人图鉴_动态绿灯」世界书，供绿灯联动使用。

插件本体随安装包分发。这个仓库的下载地址用于插件里的词库设置。

## 在插件中下载或更新词库

1. 在酒馆助手中导入并启用安装包里的 `同人图鉴_绿灯动态联动_酒馆助手一键导入_v1.7.3.json`。
2. 打开「图鉴绿灯」面板 →「⚙️ 词库设置」→「云端在线下载资料库」，填入下方的清单地址。
3. 点击「下载/更新」。插件会下载并解压词库，再保存到本地；已有词库时会先备份旧版本。

```text
https://raw.githubusercontent.com/oju706/fanwork-atlas/refs/heads/main/manifest.json
```

插件会优先尝试 jsDelivr，无法访问时会回退到 GitHub Raw。遇到下载错误时，可以先在浏览器打开上面的清单地址，并检查下方的压缩包链接能否下载。

## 数据版本和文件

初始发布版本为 `2026.11.27-v2`（2026 年 11 月 27 日，Schema 2），包含 **75,706 个角色**和 **5,966 部作品**。当前版本以 [manifest.json](manifest.json) 为准。

| 文件 | 用途 | 直链 |
| --- | --- | --- |
| `manifest.json` | 版本清单，记录版本、日期、条目数和全量包位置。 | [查看清单](https://raw.githubusercontent.com/oju706/fanwork-atlas/refs/heads/main/manifest.json) |
| `fanwork_v2.json.gz` | Gzip 压缩的完整 JSON 词库，初始版本约 5.96 MiB。 | [下载词库](https://raw.githubusercontent.com/oju706/fanwork-atlas/refs/heads/main/fanwork_v2.json.gz) |

## 维护与反馈

- 发布全量更新时，在同一次提交中更新压缩包和清单，核对 `version`、`updatedAt`、`count`、`works`、`packFile` 与 `packSizeBytes`。
- 如发现作品译名、角色归类或下载问题，请在 [Issues](https://github.com/oju706/fanwork-atlas/issues) 中提供数据版本和相关条目或报错。
- 仓库的许可文件见 [LICENSE](LICENSE)。
