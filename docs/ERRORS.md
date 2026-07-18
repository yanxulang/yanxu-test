# 错误代码

言试自产错误以`YANSHI_TEST_`开头。代码是 1.x 兼容边界，消息只用于人工诊断。

| 代码 | 含义 |
| --- | --- |
| `ASSERT` / `FAIL` | 条件断言或显式失败 |
| `EQUAL` / `NOT_EQUAL` | 普通相等关系不符 |
| `EMPTY` / `NOT_EMPTY` | 空值断言不符 |
| `DEEP_EQUAL` | 深比较发现路径化差异 |
| `APPROXIMATE` / `TOLERANCE` | 近似值不符或容差无效 |
| `CONTAINS` / `CONTAINS_TYPE` | 包含关系不符或容器类型无效 |
| `MATCH` | 正则不匹配 |
| `TYPE` / `PREDICATE` | 类型或谓词断言不符 |
| `THROWS` / `THROWS_MATCH` / `THROWS_CODE` | 操作未抛错或错误不匹配 |
| `LIMIT` / `COPY_LIMIT` / `COMPARE_LIMIT` | 参数、复制或比较预算超限 |
| `TABLE` | 表格或参数化行失败 |
| `NAME` | 套件、测试或夹具名称无效 |
| `SUITE_LIMIT` | 测试、夹具或钩子数量超限 |
| `TEST_DUPLICATE` / `FIXTURE_DUPLICATE` | 同名定义重复 |
| `FIXTURE_TYPE` / `FIXTURE_UNKNOWN` | 夹具回调或名称无效 |
| `SUITE` | `运行()`取得不成功结果 |
| `TEMP_ROOT` / `TEMP_PATH` | 临时目录根或子路径不安全 |
| `MOCK_CALL` | Mock 调用序号越界 |
| `SNAPSHOT_FILE` | 快照根文件不是 JSON 典 |
| `SNAPSHOT_MISSING` / `SNAPSHOT_MISMATCH` | 快照缺失或内容变化 |
| `HTTP_UNMATCHED` / `HTTP_BODY` | HTTP 路由未匹配或言访正文类型无效 |
| `REPOSITORY_ADAPTER` | 函数仓储回调返回形状无效 |
| `REPOSITORY_INPUT` | 仓储契约输入无效 |
| `REPOSITORY_CONTRACT` | CRUD 行为不符合契约 |
| `REPOSITORY_CLEANUP` | 契约验证后的重置失败 |

运行时、文件系统、JSON、正则、言时、言访、言库和调用方回调错误可能原样传播。用`错误详情()`读取任何错误；非言试错误会报告`YANSHI_TEST_RUNTIME`，同时保留运行时源代码、类别、位置和踪迹。
