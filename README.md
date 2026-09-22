# 每日信号文件

`signals/YYYY-MM-DD.csv` 按信号日期归档；`latest.csv` 对应最近日期。
同名 JSON 文件记录日期、行数、编码、字段及 CSV 的 SHA-256。

CSV 编码为 UTF-8 BOM，按 `signal` 降序排列。

| 字段 | 格式说明 |
|---|---|
| rank_all | 全量排名，从 1 开始 |
| date | 信号日期，YYYY-MM-DD |
| code | 六位股票代码；读取时使用文本类型，保留前导零 |
| signal | 最终分数，数值越大排名越靠前 |
| close_limit_up | 当日收盘涨停标记，True / False |
| rank_ex_limit_up | 剔除收盘涨停后的排名；被剔除行为空 |
