[返回](/README.md)

## Tabulation 组件说明

### Tabulation Attributes
|  参数   |   说明   |     类型      | 可选值 | 默认值 |
| :-----: | :------: | :-----------: | :----: | :----: |
|  width  |   宽度   | String/Number |   --   |   --   |
| loading | 加载状态 |    Boolean    |   --   | false  |

### Tabulation-column Attributes
|    参数     |                         说明                         |     类型      | 可选值 | 默认值 |
| :---------: | :--------------------------------------------------: | :-----------: | :----: | :----: |
|    label    |            标签文本，未使用则不生成该标签            |    String     |   --   |   --   |
|    value    |            内容文本，未使用则不生成该标签            | String/Number |   --   |   ''   |
| label-width |                      标签的宽度                      | String/Number |   --   |  auto  |
| value-width |                       值的宽度                       | String/Number |   --   |  auto  |
|    align    |              对齐方式 left/center/right              |    String     |   --   | center |
| label-align | 标签的对齐方式 left/center/right，未定义时使用 align |    String     |   --   | center |

### Tabulation-column Slots
| 插槽名称 |       说明       | 参数  |
| :------: | :--------------: | :---: |
|    —     | 自定义全部的内容 |  --   |
|  label   |  自定义标签区域  |  --   |
|  value   |  自定义内容区域  |  --   |