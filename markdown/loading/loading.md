[返回](/README.md)

## loading 组件说明

### loading Attributes
|         参数         |                      说明                      |     类型      | 可选值 |          默认值          |
| :------------------: | :--------------------------------------------: | :-----------: | :----: | :----------------------: |
|      v-vvc-loading       |           Loading 的显示隐藏加载状态           |    Boolean    |   --   |          false           |
|    v-vvc-loading.lock    |  v-loading 指令中的 lock 修饰符，是否锁定遮罩  |    Boolean    |   --   |          false           |
| v-vvc-loading.fullscreen | v-loading 指令中的 fullscreen 修饰符，是否全屏 |    Boolean    |   --   |          false           |
|     vvc-loading-text     |          显示在加载图标下方的加载文案          |    String     |   --   |            --            |
|   vvc-loading-spinner    |               自定义加载图标类名               |    String     |   --   |            --            |
|  vvc-loading-background  |                   遮罩背景色                   |    String     |   --   | rgba(255, 255, 255, 0.8) |
|   vvc-loading-z-index    |                   自定义层级                   | String/Number |   --   |         同 .mask         |
| vvc-loading-custom-class |              Loading 的自定义类名              |    String     |   --   |            --            |