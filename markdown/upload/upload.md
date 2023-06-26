[返回](/README.md)

## Upoad 组件说明

### Upoad Warn
v-model绑定的值可能存在base64，极大影响接口效率，触发接口前需要进行过滤。
``` javascript
fileList.map((item) => ({ fileUrl: item.fileUrl }));
```

### Upoad Attributes
|       参数       |                               说明                                |                                   类型                                    |              可选值              |  默认值   |
| :--------------: | :---------------------------------------------------------------: | :-----------------------------------------------------------------------: | :------------------------------: | :-------: |
| multipartUpload  |                            上传的方法                             |                [multipartUploadType](#multipartUploadType)                |                --                |    --     |
|      value       |                        上传的文件\文件列表                        |                               String/Array                                |                --                |    --     |
|     listType     |                          文件列表的类型                           |                                  String                                   | text/picture/picture-card/avatar |   text    |
|      accept      |     允许上传的文件类型，如 audio/*,video/*,image/*,MIME_type      |                                  String                                   |                --                |     *     |
|     multiple     |                         是否支持多选文件                          |                                  Boolean                                  |                --                |    --     |
|     lazyLoad     |                        是否开启图片懒加载                         |                                  Boolean                                  |                --                |    --     |
|     capture      |          图片选取模式，可选值为 camera (直接调起摄像头)           |                                  String                                   |                --                |    --     |
|     maxSize      |                     文件大小限制，单位为 byte                     |          Number/String/(files: [File](#paramFile)[]) => boolean           |                --                |    --     |
|     maxCount     |                         文件上传数量限制                          |                               Number/String                               |                --                |    --     |
|     disabled     |                             是否禁用                              |                                  Boolean                                  |                --                |    --     |
|     readonly     |                             是否只读                              |                                  Boolean                                  |                --                |    --     |
| previewImageOnly |                          是否可预览图片                           |                                  Boolean                                  |                --                |    true     |
|   onClickItem    |                点击文件列表中已上传的文件时的钩子                 |                    Function(item: [File](#paramFile))                     |                --                |    --     |
|     onRemove     |                     文件列表移除文件时的钩子                      |      Function(item: [File](#paramFile), list: [File](#paramFile)[])       |                --                |    --     |
|    onSuccess     |                       文件上传成功时的钩子                        |      Function(item: [File](#paramFile), list: [File](#paramFile)[])       |                --                |    --     |
|     onError      |                       文件上传失败时的钩子                        |      Function(item: [File](#paramFile), list: [File](#paramFile)[])       |                --                |    --     |
|    onProgress    |                         文件上传时的钩子                          |      Function(item: [File](#paramFile), list: [File](#paramFile)[])       |                --                |    --     |
|     onChange     |  文件状态改变时的钩子，添加文件、上传成功和上传失败时都会被调用   |      Function(item: [File](#paramFile), list: [File](#paramFile)[])       |                --                |    --     |
|   beforeUpload   |  上传文件前置钩子，返回 false 或 Promise 且被 reject，则停止上传  | Boolean/Function(files: [File](#paramFile)[], list: [File](#paramFile)[]) |                --                |    --     |
|   beforeRemove   |  删除文件前置钩子，返回 false 或 Promise 且被 reject，则停止删除  |  Boolean/Function(item: [File](#paramFile), list: [File](#paramFile)[])   |                --                |    --     |
|     onExceed     |  文件数量超出限制钩子，无返回提示Toast(`文件数量不能超过 xx个`)   |     Function(files: [File](#paramFile)[], list: [File](#paramFile)[])     |                --                |    --     |
|    onOversize    | 文件大小超出限制钩子，无返回提示Toast(`文件大小不能超过 xxKB个`)  |     Function(files: [File](#paramFile)[], list: [File](#paramFile)[])     |                --                |    --     |
|  onIllegalType   | 文件类型超出限制钩子，无返回提示Toast(`文件类型只能为 ${accept}`) |     Function(files: [File](#paramFile)[], list: [File](#paramFile)[])     |                --                |    --     |
|  deleteTrigger   |               删除功能触发逻辑，当 type=text 时可用               |                                  String                                   |       longpress/swipecell        | swipecell |
|   showFileName   |      是否展示文件名称，当 type=picture-card 或 avatar 时可用      |                                  String                                   |       longpress/swipecell        | swipecell |

### Upoad Methods
| 方法名称 |   说明   | 参数  |
| :------: | :------: | :---: |
|  submit  | 上传文件 |  --   |

### Upoad Slots
| 插槽名称 |         说明         | 参数  |
| :------: | :------------------: | :---: |
| trigger  | 触发文件选择框的内容 |  --   |
|   tip    |     提示说明文字     |  --   |

### Upoad File Type<a href="paramFile"></a>
|   参数   |                                           说明                                           |  类型  |           可选值           | 默认值 |
| :------: | :--------------------------------------------------------------------------------------: | :----: | :------------------------: | :----: |
|   name   |                                         文件名称                                         | String |             --             |   --   |
|   uuid   |                                    文件id，组件内创建                                    | String |             --             |   --   |
|   url    | 文件地址，组件内使用的文件具体地址。出于本地渲染考虑使用base64，触发接口前需要过滤该参数 | String |             --             |   --   |
| fileUrl  |                                 文件地址，必须为网络地址                                 | String |             --             |   --   |
| progress |                                    上传进度，范围0~1                                     | Number |           [0, 1]           |   --   |
| message  |                                         上传信息                                         | String |             --             |   --   |
|   type   |                                         上传信息                                         | String | pending/fulfilled/rejected |   --   |
|   补充   |                       由于使用的是{...item}，所以可自定义其他参数                        |   --   |             --             |   --   |

### multipartUpload Type<a href="paramFile"></a>
|   参数   |      说明      |            类型             | 可选值 | 默认值 |
| :------: | :------------: | :-------------------------: | :----: | :----: |
|   file   |     文件流     |            file             |   --   |   --   |
| progress |  进度条的方法  | Function(num: 上传进度0~1)  |   --   |   --   |
| success  | 上传成功的方法 | Function(url: 文件网络地址) |   --   |   --   |
|   fail   | 上传失败的方法 |          Function           |   --   |   --   |