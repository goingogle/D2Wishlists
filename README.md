# D2Wishlists - 命运2武器愿望清单

基于[凯旋丰碑](https://docs.google.com/spreadsheets/d/1JM-0SlxVDAi-C6rGVlLxa-J1WGewEeL8Qvq4htWZHhY)在线表格的 Destiny 2 武器推荐愿望清单，可直接导入 DIM（Destiny Item Manager）使用。

## 文件说明

| 文件 | 格式 | 用途 |
|---|---|---|
| `Flamia-Collection.json` | JSON | DIM 愿望清单（JSON 格式） |
| `Flamia-Collection.txt` | TXT | DIM 愿望清单（文本格式，可直接导入） |
| `weapon_hash_map.json` | JSON | 武器名称 → Hash 映射表 |
| `perk_name_hash_map.json` | JSON | Perk 名称 → Hash 映射表 |

## 数据来源

- 武器数据：Destiny 2 Bungie API（中文 Manifest）
- 推荐列表：凯旋丰碑在线 Excel 表格
- 覆盖范围：S29 赛季武器，含 PvE/PvP 推荐配置

## 导入方法

1. 打开 [DIM](https://destinyitemmanager.com)
2. 进入愿望清单（Wish Lists）设置
3. 选择导入 `Flamia-Collection.txt` 文件
4. 保存即可使用

## 更新日志

- **S29** - 从凯旋丰碑表格导入 1209 条武器推荐，覆盖 137 个武器
