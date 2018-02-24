### WBS模板数据上传协议

* **上传频率**

每日进行一次数据上传

* **消息标签**

MASTER

* **消息类型**

MASTER@WBS_TEMPLATE

* **数据协议**

```json

[
    {
        "categoryId": "2323",
        "pCategoryId": "2123123",
        "projectType": 01,
        "categoryCode": "100",
        "type": 1,
        "name": "路基清表XX桩号~XX桩号",
        "fullCode": "200-100-100-100",
        "fullName": "路基工程/土石方工程/路基清表/路基清表XX桩号~XX桩号",
        "deleted": 0
    }
]

```

| 字段名称 | 数据类型 | 字段描述 |
| :--- | :--- | :--- |
| categoryId | string | 字典ID |
| pCategoryId | string | 父字典ID |
| projectType | string | 工程类型 **见表1**|
| categoryCode | string | 字典编码 |
| type | int | 字典类型 **见表2** |
| name | string | 字典名称 |
| fullCode | string | 字典全层级编码 |
| fullName | string | 字典全层级名称 |
| deleted     | int  | 是否逻辑删除 **见表3**|

**表1** 工程类型枚举值定义

| projectType |  |
| :--- | :--- |
| 01 | 公路工程 |
| 02 | 房建工程 |
| 03 | 水利水电工程 |
| 04 | 市政工程 |
| 05 | 轨道交通 |
| 06 | 铁路工程 |
| 07 | 其他工程 |

**表2** 组织类型枚举值定义

| type |  |
| :--- | :--- |
| 0 | 单位工程 |
| 1 | 分部 |
| 2 | 分项 |
| 3 | 工序 |

**表3**  是否逻辑删除标识

| deleted |  |
| :--- | :--- |
| 0 | 未删除 |
| 1 | 已删除 |
