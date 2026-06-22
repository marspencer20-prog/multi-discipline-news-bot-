# multi-discipline-news-bot-
# 多专业新闻机器人

## 使用说明
1. 在 `config/profiles/` 下新建专业配置文件（如 `economics.yaml`）。
2. 在 `config/disciplines.py` 中添加专业词典（可选，用于自动生成关键词）。
3. 在 GitHub Secrets 中配置 `DINGTALK_WEBHOOK` 和 `GUARDIAN_API_KEY`。
4. 通过 GitHub Actions 手动选择专业运行，或等待定时触发。

## 扩展新专业
只需两步：
1. 复制 `config/profiles/economics.yaml` 并重命名。
2. 修改 `discipline` 字段，系统会自动匹配词典生成关键词。
