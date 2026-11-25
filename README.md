# 共享菜园收成波动与活动供给

重量为千克，保鲜以采收日期起的当地完整天数计。历史批次保留未成熟和已确认零收成两种状态。

## 资料

CSV 样例为合成记录，使用 UTF-8，首行为字段名。多值用竖线分隔，空单元格表示来源未填。记录日期和业务生效日期各有含义。

- beds.csv 的字段为 bed、area、shade、irrigation、square_metres。
- harvests.csv 的字段为 batch、bed、crop、plant、first、last、kg、edible_kg、state。
- scenarios.csv 的字段为 scenario、shade、from_day、yield_factor。
- menus.csv 的字段为 menu、item、crop、kg_per_group、alternatives、max_storage_days、diet。
- events.csv 的字段为 event、menu、date、groups、delivery、state、recorded。
- supplies.csv 的字段为 event、batch、kind、at、edible_kg、expires。
- purchase.csv 的字段为 offer、crop、kg_pack、cost、arrival、expiry。
- transport.csv 的字段为 delivery、leaves、arrives、kg_limit。

## 运行资料检查

在项目根目录使用 Python 3.11 或更高版本。依赖仅为标准库。

~~~sh
python3 -m compileall -q tests
python3 -m unittest discover -s tests -v
~~~
