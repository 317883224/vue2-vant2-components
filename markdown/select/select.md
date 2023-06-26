[返回](/README.md)

## Select 组件说明
[radio 单选](#radio) | [mutiple 多选](#multiple) | [concatenation 多列级联](#concatenation) | [cascade 卡片级联](#cascade)

<a id="radio"></a>
### radio 类型
#### radio Attributes
|       参数        |                      说明                      |     类型      |               可选值                |              默认值               |
| :---------------: | :--------------------------------------------: | :-----------: | :---------------------------------: | :-------------------------------: |
|       type        |                      类型                      |    String     | radio/mutiple/concatenation/cascade |               radio               |
|       value       |                     当前值                     | String Number |                 --                  |                --                 |
|       list        |    可选项数据源，键名可通过 option 属性配置    |     Array     |                 --                  |                []                 |
|      option       |                      选项                      |    Object     |                 --                  | { value: 'value', label: 'label'} |
|     disabled      |                      禁用                      |    Boolean    |                 --                  |               false               |
|     readonly      |                      只读                      |    Boolean    |                 --                  |               false               |
|   mainColorTone   |                 是否开启主色调                 |    Boolean    |                 --                  |               false               |
|    placeholder    |                     占位符                     |    String     |                 --                  |              请选择               |
| searchPlaceholder |               弹窗的输入框占位符               |    String     |                 --                  |              请输入               |
|      isLink       |         是否展示右侧箭头并开启点击反馈         |    Boolean    |                 --                  |               true                |
|      loading      |                    加载状态                    |    Boolean    |                 --                  |                --                 |
|       title       |                      标题                      |    Boolean    |                 --                  |                --                 |
|    noMatchText    |   搜索条件无匹配时显示的文字，也可以使用slot   |    String     |                 --                  |            无匹配数据             |
|    noDataText     |      选项为空时显示的文字，也可以使用slot      |    String     |                 --                  |              无数据               |
|    loadingText    |              远程加载时显示的文字              |    String     |                 --                  |              加载中               |
|    filterable     |                   是否可搜索                   |    Boolean    |                 --                  |               false               |
|    popperClass    |               Select下拉框的类名               |    String     |                 --                  |                --                 |
|      remote       |                 是否为远程搜索                 |    Boolean    |                 --                  |               false               |
|   remoteMethod    |                  远程搜索方法                  |   Function    |                 --                  |                --                 |
|     clearable     |                是否可以清空选项                |    Boolean    |                 --                  |               false               |
|    allowCreate    | 是否允许用户创建新条目，需配合 filterable 使用 |    Boolean    |                 --                  |               false               |
|   popperAppend    |         将弹出框插入至何元素，默认body         |    Boolean    |                 --                  |               body                |

#### radio Events
|    事件名称    |                   说明                   |           回调参数            |
| :------------: | :--------------------------------------: | :---------------------------: |
|     change     |           选中值发生变化时触发           |         目前的选中值          |
|     focus      |         当 input 获得焦点时触发          |              --               |
|      blur      |         当 input 失去焦点时触发          |              --               |
| visible-change |          下拉框出现/隐藏时触发           | 出现则为 true，隐藏则为 false |
|     clear      | 可清空的单选模式下用户点击清空按钮时触发 |              --               |

#### radio Methods
| 事件名称 |    说明    | 参数  |
| :------: | :--------: | :---: |
|  focus   | 打开选择器 |  --   |
|   blur   | 关闭选择器 |  --   |
|  clear   |  清除数据  |  --   |

#### radio Slots
| 事件名称 |      说明      |                                         参数                                          |
| :------: | :------------: | :-----------------------------------------------------------------------------------: |
|    --    |   展示的内容   | item: 当前选中的数据, index: 当前选中的值, value: 当前选中的值, label: 当前展示的内容 |
|  empty   | 无选项时的列表 |                  state: 类型（noMatch：无匹配数据，noData：无数据）                   |


<a id="multiple"></a>
### multiple 类型
#### multiple Attributes
|       参数        |                    说明                    |     类型      |               可选值                |                          默认值                          |
| :---------------: | :----------------------------------------: | :-----------: | :---------------------------------: | :------------------------------------------------------: |
|       type        |                    类型                    |    String     | radio/mutiple/concatenation/cascade |                          radio                           |
|       value       |                   当前值                   | string number |                 --                  |                            --                            |
|       list        |  可选项数据源，键名可通过 option 属性配置  |     Array     |                 --                  |                            []                            |
|      option       |                    选项                    |    Object     |                 --                  | { value: 'value', label: 'label', disabled: 'disabled' } |
|     disabled      |                    禁用                    |    Boolean    |                 --                  |                          false                           |
|     readonly      |                    只读                    |    Boolean    |                 --                  |                          false                           |
|    placeholder    |                   占位符                   |    String     |                 --                  |                          请选择                          |
| searchPlaceholder |             弹窗的输入框占位符             |    String     |                 --                  |                          请输入                          |
|      isLink       |       是否展示右侧箭头并开启点击反馈       |    Boolean    |                 --                  |                           true                           |
|      loading      |                  加载状态                  |    Boolean    |                 --                  |                            --                            |
|       title       |                    标题                    |    Boolean    |                 --                  |                            --                            |
|    noMatchText    | 搜索条件无匹配时显示的文字，也可以使用slot |    String     |                 --                  |                        无匹配数据                        |
|    noDataText     |    选项为空时显示的文字，也可以使用slot    |    String     |                 --                  |                          无数据                          |
|    filterable     |                 是否可搜索                 |    Boolean    |                 --                  |                          false                           |
|    popperClass    |             Select下拉框的类名             |    String     |                 --                  |                            --                            |
|     clearable     |              是否可以清空选项              |    Boolean    |                 --                  |                          false                           |
|   popperAppend    |       将弹出框插入至何元素，默认body       |    Boolean    |                 --                  |                           body                           |

#### multiple Events
|    事件名称    |                   说明                   |           回调参数            |
| :------------: | :--------------------------------------: | :---------------------------: |
|     change     |           选中值发生变化时触发           |         目前的选中值          |
|     focus      |         当 input 获得焦点时触发          |              --               |
|      blur      |         当 input 失去焦点时触发          |              --               |
| visible-change |          下拉框出现/隐藏时触发           | 出现则为 true，隐藏则为 false |
|     clear      | 可清空的单选模式下用户点击清空按钮时触发 |              --               |

#### multiple Methods
| 事件名称 |    说明    | 参数  |
| :------: | :--------: | :---: |
|  focus   | 打开选择器 |  --   |
|   blur   | 关闭选择器 |  --   |
|  clear   |  清除数据  |  --   |

#### multiple Slots
| 事件名称 |      说明      |                                           参数                                            |
| :------: | :------------: | :---------------------------------------------------------------------------------------: |
|    --    |   展示的内容   | items: 当前选中的数据, indexs: 当前选中的索引, value: 当前选中的值, label: 当前展示的内容 |
|  empty   | 无选项时的列表 |                    state: 类型（noMatch：无匹配数据，noData：无数据）                     |


<a id="concatenation"></a>
### concatenation 类型
#### concatenation Attributes
|     参数      |                       说明                       |        类型         |               可选值                |              默认值              |
| :-----------: | :----------------------------------------------: | :-----------------: | :---------------------------------: | :------------------------------: |
|     type      |                       类型                       |       String        | radio/mutiple/concatenation/cascade |              radio               |
|     value     |                      当前值                      | Array string number |                 --                  |                []                |
|     list      |                     数据列表                     |        Array        |                 --                  |                []                |
|    option     |                       选项                       |       Object        |                 --                  | [参数详情](#concatenationOption) |
|   disabled    |                       禁用                       |       Boolean       |                 --                  |              false               |
|   readonly    |                       只读                       |       Boolean       |                 --                  |              false               |
|  placeholder  |                      占位符                      |       String        |                 --                  |              请选择              |
|    isLink     |          是否展示右侧箭头并开启点击反馈          |       Boolean       |                 --                  |               true               |
|    loading    |                     加载状态                     |       Boolean       |                 --                  |              false               |
|     title     |                       标题                       |       String        |                 --                  |          请选择所在地区          |
|  noDataText   | 选项为空时显示的文字，也可以使用slot="empty"设置 |       String        |                 --                  |              无数据              |
|  popperClass  |               Select 下拉框的类名                |       String        |                 --                  |                --                |
|   clearable   |                 是否可以清空选项                 |       Boolean       |                 --                  |              false               |
| popperAppend  |          将弹出框插入至何元素，默认body          |       String        |                 --                  |               body               |
| showAllLevels |         输入框中是否显示选中值的完整路径         |       Boolean       |                 --                  |               true               |
|   separator   |                    选项分隔符                    |       String        |                 --                  |                /                 |

#### concatenation Events
|    事件名称    |                   说明                   |           回调参数            |
| :------------: | :--------------------------------------: | :---------------------------: |
|     change     |           选中值发生变化时触发           |         目前的选中值          |
|     focus      |         当 input 获得焦点时触发          |              --               |
|      blur      |         当 input 失去焦点时触发          |              --               |
| visible-change |          下拉框出现/隐藏时触发           | 出现则为 true，隐藏则为 false |
|     clear      | 可清空的单选模式下用户点击清空按钮时触发 |              --               |

#### concatenation Methods
| 事件名称 |    说明    | 参数  |
| :------: | :--------: | :---: |
|  focus   | 打开选择器 |  --   |
|   blur   | 关闭选择器 |  --   |
|  clear   |  清除数据  |  --   |

#### concatenation Slots
| 事件名称 |      说明      |                                           参数                                            |
| :------: | :------------: | :---------------------------------------------------------------------------------------: |
|    --    |   展示的内容   | items: 当前选中的数据, indexs: 当前选中的索引, value: 当前选中的值, label: 当前展示的内容 |
|  empty   | 无选项时的列表 |                    state: 类型（noMatch：无匹配数据，noData：无数据）                     |

<a id="concatenationOption"></a>
#### concatenation option Attributes
| 事件名称 |                                                说明                                                |  类型   | 可选值 |    默认    |
| :------: | :------------------------------------------------------------------------------------------------: | :-----: | :----: | :--------: |
|  value   |                                 指定选项的值为选项对象的某个属性值                                 | String  |   --   |  'value'   |
|  label   |                                 指定选项标签为选项对象的某个属性值                                 | String  |   --   |  'label'   |
| children |                               指定选项的子选项为选项对象的某个属性值                               | String  |   --   | 'children' |
| disabled |                                指定选项的禁用为选项对象的某个属性值                                | Boolean |   --   | 'disabled' |
| emitPath | 在选中节点改变时，是否返回由该节点所在的各级菜单的值所组成的数组，若设置 false，则只返回该节点的值 | Boolean |   --   |    true    |

<a id="cascade"></a>
### cascade 类型
#### cascade Attributes
|     参数      |                       说明                       |        类型         |               可选值                |     默认值     |
| :-----------: | :----------------------------------------------: | :-----------------: | :---------------------------------: | :------------: |
|     type      |                       类型                       |       String        | radio/mutiple/concatenation/cascade |     radio      |
|     value     |                      当前值                      | Array string number |                 --                  |       []       |
|     list      |                     数据列表                     |        Array        |                 --                  |       []       |
|    option     |      选项，配置选项，具体[见下表](#option)       |       Object        |                 --                  |       --       |
|   disabled    |                       禁用                       |       Boolean       |                 --                  |     false      |
|   readonly    |                       只读                       |       Boolean       |                 --                  |     false      |
|  placeholder  |                      占位符                      |       String        |                 --                  |     请选择     |
|    isLink     |          是否展示右侧箭头并开启点击反馈          |       Boolean       |                 --                  |      true      |
|    loading    |                     加载状态                     |       Boolean       |                 --                  |     false      |
|     title     |                       标题                       |       String        |                 --                  | 请选择所在地区 |
|  noDataText   | 选项为空时显示的文字，也可以使用slot="empty"设置 |       String        |                 --                  |     无数据     |
|  popperClass  |               Select 下拉框的类名                |       String        |                 --                  |       --       |
|   clearable   |                 是否可以清空选项                 |       Boolean       |                 --                  |     false      |
| popperAppend  |          将弹出框插入至何元素，默认body          |       String        |                 --                  |      body      |
| showAllLevels |         输入框中是否显示选中值的完整路径         |       Boolean       |                 --                  |      true      |
|   separator   |                    选项分隔符                    |       String        |                 --                  |       /        |

#### cascade Events
|    事件名称    |                   说明                   |           回调参数            |
| :------------: | :--------------------------------------: | :---------------------------: |
|     change     |           选中值发生变化时触发           |         目前的选中值          |
|     focus      |         当 input 获得焦点时触发          |              --               |
|      blur      |         当 input 失去焦点时触发          |              --               |
| visible-change |          下拉框出现/隐藏时触发           | 出现则为 true，隐藏则为 false |
|     clear      | 可清空的单选模式下用户点击清空按钮时触发 |              --               |

#### cascade Methods
| 事件名称 |    说明    | 参数  |
| :------: | :--------: | :---: |
|  focus   | 打开选择器 |  --   |
|   blur   | 关闭选择器 |  --   |
|  clear   |  清除数据  |  --   |

#### cascade Slots
| 事件名称 |      说明      |                                           参数                                            |
| :------: | :------------: | :---------------------------------------------------------------------------------------: |
|    --    |   展示的内容   | items: 当前选中的数据, indexs: 当前选中的索引, value: 当前选中的值, label: 当前展示的内容 |
|  empty   | 无选项时的列表 |                    state: 类型（noMatch：无匹配数据，noData：无数据）                     |

#### Option<a id="option"></a>
|     参数      |                                                说明                                                |   类型   | 可选值 |  默认值  |
| :-----------: | :------------------------------------------------------------------------------------------------: | :------: | :----: | :------: |
| checkStrictly |                                  是否严格的遵守父子节点不互相关联                                  | Boolean  |   --   |  false   |
|     value     |                                 指定选项的值为选项对象的某个属性值                                 |  String  |   --   |  value   |
|     label     |                                 指定选项标签为选项对象的某个属性值                                 |  String  |   --   |  label   |
|   disabled    |                               指定选项的子选项为选项对象的某个属性值                               |  String  |   --   | disabled |
|     lazy      |                           是否动态加载子节点，需与 lazyLoad 方法结合使用                           | Boolean  |   --   |  false   |
|   lazyLoad    |                            加载动态数据的方法，仅在 lazy 为 true 时有效                            | Function |   --   |    --    |
|     leaf      |                          指定选项的叶子节点的标志位为选项对象的某个属性值                          |  String  |   --   |   leaf   |
|   emitPath    | 在选中节点改变时，是否返回由该节点所在的各级菜单的值所组成的数组，若设置 false，则只返回该节点的值 | Boolean  |   --   |   true   |