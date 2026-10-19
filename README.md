# CC Switch 配置未生效：切换验收与回退清单

![CC Switch 配置未生效：切换验收与回退清单](cover.png)

用于验收 CC Switch 的基础供应商切换。此处不提供协议转换、自动故障切换或免费额度承诺。

## 切换前

- [ ] 软件来自 `farion1231/cc-switch` 的 Releases；官网以仓库列出的 `ccswitch.io` 为准。
- [ ] 目标 CLI 可运行。
- [ ] 已备份原连接配置，并记下当前启用项。

## 连接矩阵

| 工具 | 协议 | Orbis Base URL | 凭据 |
| --- | --- | --- | --- |
| Claude Code | Anthropic | `https://orbiorbi.com` | 对应 Claude 线路的 Key |
| Codex CLI | Responses | `https://orbiorbi.com/v1` | 对应 Responses 线路的 Key |

每个工具单独保存。模型填写所选线路的调用 ID。Claude 后台模型也要在支持范围内，后台选择主模型时考虑其费用。

## 切换后

- [ ] 确认新条目已成为当前启用项。
- [ ] 重启对应客户端。
- [ ] Claude Code 用 `/status` 核对；Codex 用演示文件读取任务验证。
- [ ] 在 Orbis 日志核对对应 Key、模型和时间。
- [ ] Windows / WSL / SSH 的运行环境与配置目录已对应。

## 没变化时的记录模板

```text
目标客户端及版本：
实际运行系统和用户目录：
CC Switch 当前启用项：
实际读取的地址及模型（不含密钥）：
Key 的站内线路：
上一次可用配置与回退位置：
```

站内修改 Key 的线路会影响其他使用同一 Key 的客户端。回退客户端配置不会自动撤销站内的线路变更；分别确认这两个位置。

## 参考资料

- [CC Switch 官方仓库与中文说明](https://github.com/farion1231/cc-switch/blob/main/README_ZH.md)
- [CC Switch 官方发布页](https://github.com/farion1231/cc-switch/releases)
- [Orbis 模型广场](https://orbiorbi.com/pricing?utm_source=github&utm_medium=article&utm_campaign=all9_20261019&utm_content=k03)

资料核对日期：2026-10-19。
