# hongqi-archiver-update

红旗分拣照片工具的**自动更新源**（公开库）。

- `latest-mac.json` — macOS 更新清单（mac 版应用「更新源地址」填它的链接）
- `latest-win.json` — Windows 更新清单（Windows 版应用填它的链接）
- `latest-mac-cn.json` / `latest-win-cn.json` — **国内网络镜像清单**：清单与安装包均走 ghproxy 镜像
  （包内容与官方 Release 完全一致，sha256 相同）。国内网络访问 GitHub 失败时，更新源改填：
  - Windows：`https://ghproxy.net/https://raw.githubusercontent.com/Blackmidoudou/hongqi-archiver-update/main/latest-win-cn.json`
  - macOS：`https://ghproxy.net/https://raw.githubusercontent.com/Blackmidoudou/hongqi-archiver-update/main/latest-mac-cn.json`
- 安装包见 [Releases](../../releases)

源代码在私有仓库 hongqi-archiver，本库仅承载发布产物。
