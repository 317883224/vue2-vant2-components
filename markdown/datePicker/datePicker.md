<!--
 * @Description: 日期选择器组件
 * @Author: YH
 * @Date: 2022-11-28 15:15:44
 * @LastEditTime: 2023-04-19 16:25:27
 * @LastEditors: FYR
 * @Reference:
-->
[返回](/README.md)

## datePicker 组件说明

### 说明
v-model绑定当前选择的日期，通过默认插槽自定义日期选择器展示的样式

### datePicker Attributes
|     参数     |                                     说明                                     |     类型      | 可选值 |       默认值        |
| :----------: | :--------------------------------------------------------------------------: | :-----------: | :----: | :-----------------: |
|    value     |                                    绑定值                                    | String/Number |   --   |         --          |
|  dateRange   |                                 是否范围选择                                 |    Boolean    |   --   |        false        |
|  separator   |                              范围选择时的分隔符                              |    String     |   --   |         至          |
|    format    |           展示的时间格式, yyyy/MM/dd hh:mm:ss 或 timestamp 时间戳            |    String     |   --   | yyyy/MM/dd hh:mm:ss |
| valueFormat  | 绑定值的时间格式, yyyy/MM/dd hh:mm:ss 或 timestamp: 时间戳 或 date：时间对象 |    String     |   --   |        date         |
| pickerFormat |    选取器的时间格式化函数(type: 当前类型, val: 当前值), 返回格式化后的值     |   Function    |   --   |         --          |
| pickerFilter |    选取器过滤函数(type: 当前类型, options: 当前值列表) 返回过滤后的值列表    |   Function    |   --   |         --          |
|     type     |         选择器类型: date time year-month month-day datehour datetime         |    String     |   --   |      datetime       |
|   minDate    |                                 最小可选时间                                 |     Date      |   --   |         --          |
|   maxDate    |                                 最大可选时间                                 |     Date      |   --   |         --          |

### datePicker Events
| 事件名称 |     说明     |            回调参数            |
| :------: | :----------: | :----------------------------: |
|  change  | 用户改变日期 | time: 日期（范围选择时为数组） |