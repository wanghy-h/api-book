### 项目清单与WBS关联数据上传协议

* **上传频率**

每1小时进行一次数据上传

* **数据协议**

```json

[
    {
        "id": "123123",
        "wbsList": [{
            "wbsId": "1321",
            "splitQuantity": 434
        }],
        "code": "34234",
        "name": "324234",
        "quantity": 1,
        "unit": "吨",
        "perPrice": 22321,
        "amount": 1,
        "deleted": false
    }
]

```

| 字段名称 | 数据类型 | 字段描述 |
| :--- | :--- | :--- |
| id | string | 清单ID |
| wbsList | list | 关联wbs节点对象列表 **见表1**|
| code | string | 项目清单编号 |
| name | string | 项目清单名称 |
| quantity | double | 数量 |
| unit | string | 单位 |
| perPrice | double | 单价 |
| amount | double | 金额 |
| deleted | boolean | 逻辑删除标志 **见表2** |

**表1** 关联wbs节点对象列表

| 字段名称 | 数据类型 | 字段描述 |
| :--- | :--- | :--- |
| wbsId | string | wbs节点ID |
| splitQuantity | double | 拆分量 |

**表2** 逻辑删除标志位枚举值定义

| deleted |  |
| :--- | :--- |
| false | 未删除 |
| true | 已删除 |