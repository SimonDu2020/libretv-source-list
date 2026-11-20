# LibreTV 双源合集

一个订阅链接导入 34 个点播接口和 16 个直播播放列表，与当前 LibreTV App 中使用的合并配置一致。

2026-11-20 更新：在原有 39 个点播源基础上，并入手工地址列表并逐个实测筛选，只保留 `?ac=list` 能返回非空 `list` 的接口；直播源新增 iptv-org 的海外频道（英语 / 美国 / 英国 / 加拿大 / 澳洲 / 日本 / 韩国，以及电影、新闻、体育、纪录片、少儿、娱乐、音乐分类）。

## 固定订阅地址

```text
https://raw.githubusercontent.com/haojun19980728-prog/libretv-source-list/main/libretv-sources.json
```

在 LibreTV 的「设置 → 数据源 → 数据源订阅」中粘贴上述地址，点击「添加并同步」。看到「34 个点播源、16 个直播源」即表示配置导入完成。该文件为 LibreTV-SourceList 格式，不是「配置导入导出」中的整机备份文件。

这个链接指向同一个文件。后续更新仓库中的 `libretv-sources.json` 后，在 App 中重新同步即可，无需更换订阅地址。此仓库没有定时抓取上游的任务，不会自动跟随上游变化。

## 来源与版本

本次配置整理日期为 2026-11-20；在 2026-10-15 快照基础上，对全部地址做了可用性实测并新增海外直播源。

- [ljfbin2/tv-sources](https://github.com/ljfbin2/tv-sources)，提交 `747e102e5ef36726fc78ba33ccd73b1d4b21b97d`
- [ximishan/LibreTV-api-source](https://github.com/ximishan/LibreTV-api-source)，提交 `bc9d43b08da0b22e01c67264b323ebf1930a1b97`

已用当前 App 的订阅解析器校验：34 个点播源、16 个直播源，无跳过或截断。每个点播接口均已实测 `?ac=list` 返回有效 JSON 且 `list` 非空；未验证具体媒体内容能否播放。GitHub 原始文件地址能否访问取决于使用者的网络。

本仓库保存接口地址配置，不存储媒体文件。第三方服务及内容的权利归其权利人所有；公开接口或开源配置不代表取得内容使用授权。请仅使用获得许可的服务与内容。
