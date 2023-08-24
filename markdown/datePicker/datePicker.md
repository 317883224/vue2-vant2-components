<!--
 * @Description: 日期选择器组件
 * @Author: YH
 * @Date: 2022-11-28 15:15:44
 * @LastEditTime: 2023-08-24 17:24:07
 * @LastEditors: FYR
 * @Reference:
-->
[返回](/README.md)

## datePicker 组件说明

### 说明
v-model绑定当前选择的日期，通过默认插槽自定义日期选择器展示的样式

### datePicker Attributes
|       参数        |                                     说明                                     |          类型           | 可选值 |                                  默认值                                   |
| :---------------: | :--------------------------------------------------------------------------: | :---------------------: | :----: | :-----------------------------------------------------------------------: |
|       value       |                                    绑定值                                    | String / Number / Array |   --   |                                    --                                     |
|    date-range     |                                 是否范围选择                                 |         Boolean         |   --   |                                   false                                   |
|     separator     |                              范围选择时的分隔符                              |         String          |   --   |                                    至                                     |
|      format       |           展示的时间格式, yyyy/MM/dd hh:mm:ss 或 timestamp 时间戳            |         String          |   --   |                            yyyy/MM/dd hh:mm:ss                            |
|   value-format    | 绑定值的时间格式, yyyy/MM/dd hh:mm:ss 或 timestamp: 时间戳 或 date：时间对象 |         String          |   --   |                                   date                                    |
|   picker-format   |    选取器的时间格式化函数(type: 当前类型, val: 当前值), 返回格式化后的值     |        Function         |   --   |                                    --                                     |
|   picker-filter   |    选取器过滤函数(type: 当前类型, options: 当前值列表) 返回过滤后的值列表    |        Function         |   --   |                                    --                                     |
|       type        |         选择器类型: date/time/year-month/month-day/datehour/datetime         |         String          |   --   |                                   date                                    |
|     min-date      |                                 最小可选时间                                 |          Date           |   --   |                                    --                                     |
|      loading      |                                   加载状态                                   |         Boolean         |   --   |                                   false                                   |
|    placeholder    |                            非范围选择时的占位内容                            |         String          |   --   |                                "选择日期"                                 |
| start-placeholder |                         范围选择时开始日期的占位内容                         |         String          |   --   |                                "开始日期"                                 |
|  end-placeholder  |                         范围选择时结束日期的占位内容                         |         String          |   --   |                                "结束日期"                                 |
|     clearable     |                               是否显示清除按钮                               |         Boolean         |   --   |                                   false                                   |
|    prefix-icon    |                             自定义头部图标的类名                             |         String          |   --   | "https://mw-crm-file.oss-cn-shenzhen.aliyuncs.com/projectImages/icon.png" |
|    clear-icon     |                             自定义清空图标的类名                             |         String          |   --   |                                  "close"                                  |
| show-picker-icon  |                              是否显示选择器图标                              |         Boolean         |   --   |                                   false                                   |
|  picker-options   |            当前时间日期选择器特有的选项参考[下表](#pickerOptions)            |         Object          |   --   |                                    {}                                     |

### datePicker Events
| 事件名称 |     说明     |            回调参数            |
| :------: | :----------: | :----------------------------: |
|  change  | 用户改变日期 | time: 日期（范围选择时为数组） |

<a id="pickerOptions"></a>
### picker-options
|    参数     |                                  说明                                   |   类型   | 可选值 |   默认值   |
| :---------: | :---------------------------------------------------------------------: | :------: | :----: | :--------: |
|  shortcuts  | 设置快捷选项，需要传入 { text, onClick } 对象用法参考[下表](#shortcuts) | Object[] |   --   |     --     |
| placeholder |                            选择时的占位内容                             |  String  |   --   | "快捷选项" |

<a id="shortcuts"></a>
### shortcuts
|  参数   |                   说明                    |   类型   | 可选值 | 默认值 |
| :-----: | :---------------------------------------: | :------: | :----: | :----: |
|  text   |                 标题文本                  |  string  |   --   |   --   |
| onClick | 选中后的回调函数，返回需要绑定的 value 值 | function |   --   |   --   |