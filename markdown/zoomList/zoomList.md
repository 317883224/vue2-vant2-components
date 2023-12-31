[返回](/README.md)

## zoomList 组件说明
需要搭配[zoomItem](#zoomItem)一起使用

### zoomList Attributes
|  参数  | 说明  |  类型  | 可选值 | 默认值 |
| :----: | :---: | :----: | :----: | :----: |
| width  | 宽度  | string |   --   |   --   |
| height | 高度  | string |   --   |   --   |

### zoomList Events
| 事件名称 |     说明     |     回调参数     |
| :------: | :----------: | :--------------: |
|  scroll  | 实时滚动位置 | { y: y轴滚动值 } |

### zoomList Methods
|  方法名称  |                           说明                            |                                      参数                                       |
| :--------: | :-------------------------------------------------------: | :-----------------------------------------------------------------------------: |
|  backTop   |                         回到顶部                          |                                       --                                        |
| stopScroll |                         停止滚动                          | 可传入一个boolean值，false: 在当前位置停止(默认) true: 在惯性滚动的终点位置停止 |
|  doLayout  | 重新计算布局 (异步加载数据，元素从隐藏变成显示时需要用到) |                              可传入一个初始缩放值                               |

### zoomList Slots
| 插槽名称 |                  说明                   | 参数  |
| :------: | :-------------------------------------: | :---: |
|    --    | 展示的内容，只能是[zoomItem](#zoomItem) |  --   |

### zoomItem Attributes<a id="zoomItem"></a>
|       参数       |     说明     |     类型      |                      可选值                      | 默认值 |
| :--------------: | :----------: | :-----------: | :----------------------------------------------: | :----: |
|      width       |     宽度     |    string     |                        --                        |   --   |
|      height      |     高度     |    string     |                        --                        |   --   |
|     disabled     | 是否禁用缩放 |    boolean    |                        --                        |   --   |
|   defaultScale   |   默认缩放   | string,number | auto: 宽度自适应(默认), 输入数字: 代表具体缩放值 |  auto  |
|       min        |   最小缩放   |    number     |                        --                        |   1    |
|       max        |   最大缩放   |    number     |                        --                        |   5    |
| doubleClickScale | 双击放大缩小 |    boolean    |                        --                        |   --   |