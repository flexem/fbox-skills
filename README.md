# FBox Skills

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

FBox 工业物联网 Claude 技能集合，提供 MCP 和 CLI 两种方式管理设备。

## 包含的技能

| 技能 | 说明 | 版本 |
|------|------|------|
| [fboxmcp](fboxmcp/) | FBox 设备管理（MCP） — 设备状态、监控点读写、报警处理、历史数据、远程控制 | 0.1.4 |
| [fboxcli](fboxcli/) | FBox 设备管理（CLI） — 命令行工具，支持自动化脚本和批量运维 | 0.1.0 |

## 快速安装

```bash
# 设置 API Key
export FBOXMCP_API_KEY=sk-xxxxxx

# 添加 MCP Server
claude mcp add --transport http fboxmcp https://fboxmcp.fbox360.com \
  --header "Authorization: Bearer ${FBOXMCP_API_KEY}"

# 安装插件
claude plugin marketplace add https://github.com/flexem/fbox-skills
claude plugin install fboxmcp
```

各技能的详细安装说明请参考对应目录下的 INSTALL.md。

## 仓库结构

```
fbox-skills/
├── .claude-plugin/
│   └── marketplace.json    # 插件市场配置
├── fboxmcp/                # FBox 设备管理技能（MCP）
│   ├── SKILL.md            # 技能规则定义
│   ├── README.md           # 技能说明
│   ├── INSTALL.md          # 安装指南
│   └── references/         # 工具参考文档
└── fboxcli/                # FBox 设备管理技能（CLI）
    ├── SKILL.md            # 技能规则定义
    ├── README.md           # 技能说明
    ├── INSTALL.md          # 安装指南
    └── references/         # 命令参考文档
```

## 许可证

MIT License

## 联系方式

- 官网: [https://fbox360.com](https://fbox360.com)
- 作者: flexem
- 问题反馈: [GitHub Issues](https://github.com/flexem/fbox-skills/issues)
