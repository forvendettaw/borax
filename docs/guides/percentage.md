# percentage 模块

> 模块： `borax.structures.percentage`

## 创建数据对象

该模块仅定义一个 `Percentage` 类，表示具体的百分比数据。类 `__init__` 函数定义如下：

```python
def __init__(self, *, total=100, completed=0, places=2, display_fmt='{completed} / {total}'):
  pass
```

各参数意义如下：

| 参数 | 数据类型 | 意义 |
| ------ | ------ | ------ |
| total | int | 总数 |
| completed | int | 完成数目 |
| places | int | 百分比的小数点，如 place=2，时显示为 34.56% |
| display_fmt | string | 显示格式字符串，可用变量：total, completed |

## 数据属性

`Percentage` 包含了一系列的数据属性。

```python
from borax.structures.percentage import Percentage

p = Percentage(total=100, completed=34)

```

包含以下数据属性。

| 属性 | 数据类型 | 描述 | 示例 |
| ------ | ------ | ------ | ------ |
| total | int | 总数 | `100` |
| completed | int | 完成数目 | `34` |
| percent | float | 百分比数值 | `0.34` |
| percent_display | string | 百分比字符串 | `'34.00%'` |
| display | string | 进度字符串 |  `'34 / 100'`|

## 方法

- **`increase(value=1)`**

增加进度值，默认间隔为1

- **`decrease(value=1)`**

减少进度值，默认为1

- **`as_dict(prefix='')`**

导出字典格式，`prefix` 为键(key)的前缀。

