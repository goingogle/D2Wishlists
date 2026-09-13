# D2Wishlists - 命运2武器愿望清单

基于[小棒猪-LGpig 的 PVE 购物清单](https://starside.work/pve-farming/index.html)（Starside by 日栎w，数据源为[凯旋丰碑 Destiny 2: Endgame Analysis](https://docs.google.com/spreadsheets/d/1JM-0SlxVDAi-C6rGVlLxa-J1WGewEeL8Qvq4htWZHhY) 在线表格）的 Destiny 2 武器推荐愿望清单，可直接导入 DIM（Destiny Item Manager）使用。

## 文件说明

| 文件 | 格式 | 用途 |
|---|---|---|
| `Flamia-Collection.json` | JSON | 愿望清单结构化数据（hash + 插件组合 + 评级） |
| `Flamia-Collection.txt` | TXT | DIM 愿望清单（文本格式，可直接导入） |
| `weapon_hash_map.json` | JSON | 武器名称 → Hash 映射表（含同名复刻/精选版本） |
| `perk_name_hash_map.json` | JSON | Perk 名称 → Hash 映射表（含全部同义 hash） |

## 数据来源

- 武器数据：Destiny 2 Bungie API（中文 Manifest 244213.26.06.29.2000-1）
- 推荐列表：Starside 购物清单-白弹 / 绿弹 / 威能 / 其他（小棒猪-LGpig）
- 覆盖范围：白弹 356 + 绿弹 228 + 威能 156 + 其他 8，共 748 把传说武器的完整 Perk 推荐

## 愿望单格式说明

- 每行 `dimwishlist:item=<武器hash>&perks=<插件hash列表>` 为一组完整推荐组合：枪管 / 弹匣 / 特性1 / 特性2，按清单页面上的优先级从高到低全排列，文件内第一组即全首选组合
- Perk 使用普通版 hash，DIM 匹配时强化 Perk / 强化枪管弹匣自动视为等价
- 同名武器的复刻 / 精选版本（如「猛攻版本」「玖的仪式版本」）hash 已逐行覆盖，两个版本均可命中
- 页面标注删除线（已不可获取）的 Perk 已剔除
- 评级为同类武器内排名（S / A / B / C），已写入 notes 与 JSON 的 `tags`

## 导入方法

1. 打开 [DIM](https://destinyitemmanager.com)
2. 进入愿望清单（Wish Lists）设置
3. 选择导入 `Flamia-Collection.txt` 文件
4. 保存即可使用

## 更新日志

- **2026-09-13** - 升级为购物清单全量版本：748 把武器 / 8412 条组合（白弹 2946 + 绿弹 2090 + 威能 3131 + 其他 245），基于 Bungie 中文 Manifest 重新解析全部武器与 Perk hash；合并刷取清单（白弹紫枪/绿弹紫枪/威能紫枪）的 T 档评级、类型评级与评级理由至 216 把武器的 notes；同步重建两个 hash 映射表；移除旧 CSV 源表（内容已被购物清单全量覆盖）
- **S29** - 从凯旋丰碑表格导入 1209 条武器推荐，覆盖 137 个武器
