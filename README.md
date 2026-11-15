# hongqi-archiver-update

红旗分拣照片工具的**自动更新源**（公开库）。

- `latest-mac.json` — macOS 更新清单（mac 版应用「更新源地址」填它的链接）
- `latest-win.json` — Windows 更新清单（Windows 版应用填它的链接）
- `latest-mac-cn.json` / `latest-win-cn.json` — **国内网络镜像清单**：清单与安装包均走 ghproxy 镜像
  （包内容与官方 Release 完全一致，sha256 相同）。国内网络访问 GitHub 失败时，更新源改填：
  - Windows：`https://ghproxy.net/https://raw.githubusercontent.com/Blackmidoudou/hongqi-archiver-update/main/latest-win-cn.json`
  - macOS：`https://ghproxy.net/https://raw.githubusercontent.com/Blackmidoudou/hongqi-archiver-update/main/latest-mac-cn.json`
  - 备用镜像（gh-proxy）：Windows `https://gh-proxy.com/https://raw.githubusercontent.com/Blackmidoudou/hongqi-archiver-update/main/latest-win-cn2.json`，
    macOS `.../latest-mac-cn2.json`；清单也可走 jsDelivr：
    `https://cdn.jsdelivr.net/gh/Blackmidoudou/hongqi-archiver-update@main/latest-win-cn2.json`
- `latest-mac-gitee.json` — **macOS 的 Gitee 清单**：清单与安装包均在 Gitee，国内直连无需代理
  - 更新源填：`https://gitee.com/black-mi/hongqi-archiver-update/raw/main/latest-mac-gitee.json`
  - 安装包托管在 Gitee 发行版附件（免登录下载），sha256 与官方 Release 一致
- `latest-win-gitee.json` — **Windows 的 Gitee 清单**（v1.18.0 起）
  - 更新源填：`https://gitee.com/black-mi/hongqi-archiver-update/raw/main/latest-win-gitee.json`
  - v1.18.0 起 Windows 包瘦身到 53MB（原 164.5MB），已可托管在 Gitee
- 安装包见 [Releases](../../releases)

## Gitee 镜像（国内推荐）

GitHub 镜像库：`https://gitee.com/black-mi/hongqi-archiver-update`

| 用途 | 地址 |
| --- | --- |
| macOS 清单 | `https://gitee.com/black-mi/hongqi-archiver-update/raw/main/latest-mac-gitee.json` |
| Windows 清单 | `https://gitee.com/black-mi/hongqi-archiver-update/raw/main/latest-win-gitee.json` |
| 安装包 | 见 Gitee [发行版](https://gitee.com/black-mi/hongqi-archiver-update/releases) |

> Windows 包在 v1.18.0 起瘦身到 **53MB**（原来 164.5MB，原因是捆绑了上游全量 ffmpeg
> 构建，各 162MB）。现已可托管在 Gitee，`latest-win-gitee.json` 即国内直连线路。
> 更早版本（≤1.17.0）的 Windows 包仍只能走 `latest-win-cn.json`（ghproxy 镜像）。

实测下载速度：Gitee 约 2.1MB/s，ghproxy 约 0.37MB/s。

源代码在私有仓库 hongqi-archiver，本库仅承载发布产物。
