# Contributing

感谢你改进 Journal Academic Audit Skill。

## 提交前

1. 先搜索已有 Issue，避免重复工作；较大改动建议先开 Issue 说明目标、证据和兼容影响。
2. 不要提交论文全文、付费数据库导出、用户报告、个人信息、凭证、Cookie、令牌、本机绝对路径或未经授权的第三方内容。
3. 修改规则时同时检查 `SKILL.md`、相关 `references/` 和验证脚本，避免文档与机器校验不一致。
4. 保持跨 Agent 可移植性；平台专属元数据不得改变规范工作流或放宽安全边界。

## 本地验证

从 `journal-academic-audit` 目录运行：

```bash
python3 scripts/audit_run.py --self-test
python3 scripts/security_scan.py --self-test
python3 scripts/security_scan.py . --profile package
```

如果修改了示例审计包，还应运行对应模式的 `audit_run.py` 和 `security_scan.py --profile output`。Pull Request 应说明改动目的、验证结果和任何兼容性影响。

## 贡献许可

提交贡献即表示你确认拥有相应权利，并同意按 Apache License 2.0 将贡献提供给本项目。不要提交与该许可不兼容或来源不明的内容。

## 行为与安全

保持讨论专业、具体并尊重他人。安全漏洞、凭证暴露或隐私风险请遵循 [SECURITY.md](SECURITY.md)，不要在公开 Issue 中披露可利用细节或敏感数据。
