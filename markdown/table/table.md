[返回](/README.md)

## Table 组件说明

### Table Attributes
|           参数           |                                            说明                                             |                         类型                          |    可选值     |  默认值   |
| :----------------------: | :-----------------------------------------------------------------------------------------: | :---------------------------------------------------: | :-----------: | :-------: |
|          width           |                                          表格宽度                                           |                     String/Number                     |      --       |    --     |
|          height          |                                          表格高度                                           |                     String/Number                     |      --       |    --     |
|        max-height        |                   Table 的最大高度。合法的值为数字或者单位为 px 的高度。                    |                     String/Number                     |      --       |    --     |
|           data           |                                         显示的数据                                          |                     String/Number                     |      --       |    --     |
|           color          |                                           字体颜色                                          |                         String                        |      --       |    --     |
|    header-background     |                                          表头颜色                                           |                        String                         |      --       |  #ff711b  |
|   header-border-color    |                                        表头边框颜色                                         |                        String                         |      --       |   #fff    |
|       header-color       |                                        表头字体颜色                                         |                        String                         |      --       |   #fff    |
|          border          |                                        是否需要边框                                         |                        Boolean                        |      --       |   true    |
|       border-color       |                                          边框颜色                                           |                        String                         |      --       | #dcdfe680 |
|      border-radius       |                                            圆角                                             |                     String/Number                     |      --       |    --     |
|          rowKey          |                             行数据的 Key，用来优化 Table 的渲染                             |                     String/Number                     |      --       |    --     |
|        empty-text        |                    空数据时显示的文本内容，也可以通过 slot="empty" 设置                     |                        String                         |      --       | 暂无数据  |
| highlight-current-select |                                       是否要高亮选中                                        |                        Boolean                        |      --       |   false   |
| highlight-current-select-color |                                 高亮选中颜色                                        |                        String                        |      --       |   #ff711b0d   |
|       show-header        |                                        是否显示表头                                         |                        Boolean                        |      --       |   true    |
|         loading          |                   是否加载状态，加载过程中不触发load事件，必须使用sync修饰符                   |                        Boolean                        |      --       |   false   |
|       loading-text       |                                     加载过程中的提示文案                                     |                        String                        |      --       |  加载中... |
|          error           |          是否加载失败，加载失败后点击错误提示可以触发error-load事件，必须使用sync修饰符          |                        Boolean                        |      --       |   false   |
|        error-text        |                                     加载失败后的提示文案                                   |                        String                        |      --    | 网络繁忙，请稍后重试！ |
|         finished         |                          是否已加载完成，加载完成后不再触发load事件                           |                        Boolean                        |      --       |   true   |
|       finished-text      |                                    加载完成后的提示文案                                     |                        String                        |       --       |     --     |
|       hint-type          | 提示类型，mask：遮罩 text：文字 all：遮罩+文字 fucs：第一次加载时是遮罩后续为文字 card：一直展示遮罩 |                    String                         | mask/text/all/fuse |   all    |
|       span-method        |                                    合并行或列的计算方法                                     |   Function({ row, column, rowIndex, columnIndex })    |      --       |    --     |
|       show-summary       |                                    是否在表尾显示合计行                                     |                        Boolean                        |      --       |   false   |
|         sumText          |                                     合计行第一列的文本                                      |                        String                         |      --       |   合计    |
|      summary-method      |                                    自定义的合计计算方法                                     |              Function({ columns, data })              |      --       |    --     |
|   current-select-value   |                               当前选中的值，type=select时使用                               |                         Array                         |      --       |    --     |
|       default-sort       |     默认的排序列的 prop 和顺序。它的prop属性指定默认的排序的列，order指定默认排序的顺序     |                        Object                         |      --       |    {}     |
|          stripe          |                                     是否为斑马纹 table                                      |                        Boolean                        |      --       |   false   |
|  header-row-class-name   |     表头行的 className 的回调方法，也可以使用字符串为所有表头行设置一个固定的 className     |           Function({row, rowIndex})/String            |      --       |    --     |
|     header-row-style     |     表头行的 style 的回调方法，也可以使用一个固定的 Object 为所有表头行设置一样的 Style     |           Function({row, rowIndex})/Object            |      --       |    --     |
|  header-cell-class-name  | 表头单元格的 className 的回调方法，也可以使用字符串为所有表头单元格设置一个固定的 className | Function({row, column, rowIndex, columnIndex})/String |      --       |    --     |
|    header-cell-style     | 表头单元格的 style 的回调方法，也可以使用一个固定的 Object 为所有表头单元格设置一样的 Style | Function({row, column, rowIndex, columnIndex})/Object |      --       |    --     |
|      row-class-name      |         行的 className 的回调方法，也可以使用字符串为所有行设置一个固定的 className         |           Function({row, rowIndex})/String            |      --       |    --     |
|        row-style         |         行的 style 的回调方法，也可以使用一个固定的 Object 为所有行设置一样的 Style         |           Function({row, rowIndex})/Object            |      --       |    --     |
|     cell-class-name      |     单元格的 className 的回调方法，也可以使用字符串为所有单元格设置一个固定的 className     | Function({row, column, rowIndex, columnIndex})/String |      --       |    --     |
|        cell-style        |     单元格的 style 的回调方法，也可以使用一个固定的 Object 为所有单元格设置一样的 Style     | Function({row, column, rowIndex, columnIndex})/Object |      --       |    --     |
|        class-name        |                                       列的 className                                        |                        String                         |      --       |    --     |
|     label-class-name     |                              当前列标题的自定义类名 className                               |                        String                         |      --       |    --     |
|           move           |                         是否可滑动，一般为多数据需要滚动加载时需要                          |                        Boolean                        |      --       |   true    |
|          offset          |                         滚动条与底部距离小于 offset 时触发load事件                          |                        Number                         |      --       |    100    |
|        errorImage        |                 错误状态的图片，默认继承 Vue.prototype.$VVC_ERRORIMAGE                    |                        String                         |      --       |  $VVC_ERRORIMAGE  |
|        emptyImage        |                 无数据状态图片，默认继承 Vue.prototype.$VVC_ERRORIMAGE                    |                        String                         |      --       |  $VVC_EMPTYIMAGE  |
|      finishedImage       |               无更多数据状态图片，默认继承 Vue.prototype.$VVC_ERRORIMAGE                |                        String                         |      --       |  $VVC_FINISHEDIMAGE  |

### Table Events
|     事件名称     |                     说明                     |                回调参数                |
| :--------------: | :------------------------------------------: | :------------------------------------: |
|   header-click   |      当某一列的表头被点击时会触发该事件      |            column, colIndex            |
|    cell-click    |       当某个单元格被点击时会触发该事件       | row, column, rowIndex, colIndex, event |
|    row-click     |         当某一行被点击时会触发该事件         |          row, rowIndex, event          |
|       load       |                   触底事件                   |                   --                   |
|     loading      |                   加载事件                   |                   --                   |
|      select      | 当用户手动勾选数据行的 Checkbox 时触发的事件 |    selection, row, rowIndex, event     |
|    select-all    |   当用户手动勾选全选 Checkbox 时触发的事件   |               selection                |
| selection-change |        当选择项发生变化时会触发该事件        |               selection                |
|   sort-change    |  当表格的排序条件发生变化的时候会触发该事件  |        { column, prop, order }         |
|   error-load    |         加载失败后点击错误提示时触发         |        { column, prop, order }         |

### Table Methods
|      方法名称      |                                                    说明                                                     |            参数             |
| :----------------: | :---------------------------------------------------------------------------------------------------------: | :-------------------------: |
|      doLayout      |             对 Table 进行重新布局。当 Table 或其祖先元素由隐藏切换为显示时，可能需要调用此方法              |             --              |
|   clearSelection   |                                        用于多选表格，清空用户的选择                                         |             --              |
| toggleRowSelection | 用于多选表格，切换某一行的选中状态，如果使用了第二个参数，则是设置这一行选中与否（selected 为 true 则选中） |     rowIndex, selected      |
| toggleAllSelection |                                     用于多选表格，切换所有行的选中状态                                      |             --              |
|     clearSort      |                                 用于清空排序条件，数据会恢复成未排序的状态                                  |             --              |
|        sort        |                      手动对 Table 进行排序。参数prop属性指定排序列，order指定排序顺序                       | prop: string, order: string |

### Table-column Slots
| 插槽名称 |    说明    | 参数  |
| :------: | :--------: | :---: |
|   hint   | 自定义提示 |  --   |

### Table-column Attributes
|        参数         |                                                    说明                                                     |                    类型                    |      可选值       | 默认值 |
| :-----------------: | :---------------------------------------------------------------------------------------------------------: | :----------------------------------------: | :---------------: | :----: |
|        type         |    对应列的类型。如果设置了 selection 则显示多选框；如果设置了 index 则显示该行的索引（从 1 开始计算）；    |               String/Number                |        --         |   --   |
|        width        |                                                对应列的宽度                                                 |               String/Number                |        --         |   --   |
|      minWidth       | 对应列的最小宽度，与 width 的区别是 width 是固定的，min-width 会把剩余宽度按比例分配给设置了 min-width 的列 |               String/Number                |        --         |   --   |
|        label        |                                                 显示的标题                                                  |                   String                   |        --         |   --   |
|        prop         |                                             对应列内容的字段名                                              |                   String                   |        --         |   --   |
|        align        |                                                  对齐方式                                                   |                   String                   | left/center/right |  left  |
|     headerAlign     |                              表头对齐方式，若不设置该项，则使用表格的对齐方式                               |                   String                   | left/center/right |  left  |
|      formatter      |                                                 格式化内容                                                  | Function(row, column, cellValue, colIndex) |        --         |   --   |
| showOverflowTooltip |                                       当内容过长被隐藏时显示 tooltip                                        |                  Boolean                   |        --         | false  |
|        fixed        |                                列是否固定在左侧或者右侧，true 表示固定在左侧                                |              String, Boolean               | true, left, right |   --   |
|      sortable       |                           对应列是否可以排序，需要监听 Table 的 sort-change 事件                            |                  Boolean                   |        --         | false  |

### Table-column Slots
| 插槽名称 |       说明       |                  参数                   |
| :------: | :--------------: | :-------------------------------------: |
|    —     |  自定义列的内容  | { row, column, \$rowIndex, \$colIndex } |
|  header  | 自定义表头的内容 |          { column, $colIndex }          |