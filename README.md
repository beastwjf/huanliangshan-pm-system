# 环两山项目管理配置备份仓库

本仓库用于备份「环两山联合会 AI 项目管理」系统的配置数据，包括：

- `projects.json`：项目注册表（所有项目的索引，不存敏感数据）
- `sop/`：可复用的 SOP 文档（Markdown 格式）
- `workflows/`：飞书自动化工作流配置备份
- `reports/`：项目复盘报告存档（非敏感版本）

## 数据说明

| 文件 | 用途 | 更新频率 |
|---|---|---|
| `projects.json` | 项目索引表，串联飞书台账与项目库 | 每新增项目时更新 |
| `sop/*.md` | 系统固化后导出的 Skill 文本 | 系统跑通后一次写入 |
| `workflows/*.json` | 飞书自动化规则备份 | 配置变更时同步 |
| `reports/*.md` | 复盘报告存档 | 每个项目结项后归档 |

## 安全说明

- 本仓库 **Private**，不公开
- 不含任何 API Secret、财务明细、个人联系方式
- 飞书 App Secret 通过环境变量管理，不进版本库

## 快速使用

```bash
# 克隆仓库
git clone git@github.com:beastwjf/huanliangshan-pm-system.git
cd huanliangshan-pm-system

# 更新项目注册表后推送
git add projects.json
git commit -m "feat: 新增项目 [项目ID]"
git push
```
