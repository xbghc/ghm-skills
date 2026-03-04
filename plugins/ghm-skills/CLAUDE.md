## 维护说明

### plugin.json 动态更新

每次添加、修改或删除 skill 时，同步更新 `.claude-plugin/plugin.json` 中的 `description` 和 `keywords` 字段，使其准确反映当前包含的所有 skill 的功能范围。

### prompt-guide.md 定期更新

定期访问 Stitch 官方提示词指南 https://stitch.withgoogle.com/docs/learn/prompting/ ，将最新的最佳实践同步到 `skills/stitch-ui/references/prompt-guide.md` 中。
