### 项目WBS数据上传协议

* **上传频率**

每1小时进行一次数据上传

* **消息标签**

MASTER

* **消息类型**

MASTER@PROJECT_WBS

* **数据协议**

```json

[
    {
        "wbsId": "123123",
        "pWbsId": "34234",
        "code":"1010",
        "wbsName":"底基层",
        "categoryId": "12",
        "categoryCode": "101212",
        "type": 1,
        "designCount": 314,
        "beginStakeNo": 324.23,
        "endStakeNo": 32423.4,
        "unit": "吨",
        "amount": 3434,
        "deleted": false
    }
]

```

| 字段名称 | 数据类型 | 字段描述 |
| :--- | :--- | :--- |
| wbsId | string | wbs节点ID |
| pWbsId | string | wbs父节点ID |
| wbsCode | string | wbs节点编号 |
| wbsName | string | wbs父节点名称 |
| categoryId | string | 模板wbsID |
| categoryCode | string | 模板wbsb编号 |
| type | int | 字典类型 **见表1** |
| beginStakeNo | double | 开始桩号 |
| endStakeNo | double | 结束桩号 |
| designCount | double | 设计量 |
| unit | string | 单位 |
| amount | double | 金额 |
| deleted | boolean | 逻辑删除标志位 **见表2**|


**表1** 组织类型枚举值定义

| type |  |
| :--- | :--- |
| 0 | 单位工程 |
| 1 | 分部 |
| 2 | 分项 |
| 3 | 工序 |

**表2** 逻辑删除标志位枚举值定义

| deleted |  |
| :--- | :--- |
| false | 未删除 |
| true | 已删除 |

