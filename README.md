一. 小沃目前支持接入Home Assistant的产品有：

- 小沃精灵
- 小沃精灵S1
- 星联网关
- 小融网关
- 小沃壁挂炉
- 星联网关已完成适配的第三方壁挂炉



二. 接入步骤：

1. 通过应用市场下载并安装小沃云家App（Android和iOS都可以），通过手机号完成登录与绑定设备操作。

2. 点击 ([获取授权码](https://www.baidu.com)) 链接，通过手机号（注：输入的手机号需与步骤1的登录手机号一致）获取授权码，保存获取到的授权码。

3. 将ciaowarm文件夹复制到Home Assistant的custom_components文件夹下，并重启Home Assistant。

4. 点击Home Assistant左侧导航栏“配置”，点击"设备与服务"，点击右下角的“添加集成”，选择“Ciaowarm”品牌，在上面的输入框内输入步骤1和2所用的手机号，在下面的输入框内输入步骤2获取到的授权码，点击“提交”，即可完成接入。

   

三. 支持的参数：

1. 温控器：

   |      参数名      | 操作权限 |
   | :--------------: | :------: |
   |      网关ID      |   只读   |
   |     温控器ID     |   只读   |
   |  温控器在线状态  |   只读   |
   |    温控器名称    |   只读   |
   |     室内温度     |   只读   |
   | 离家模式目标温度 |  可读写  |
   | 居家模式目标温度 |  可读写  |
   | 睡眠模式目标温度 |  可读写  |
   |       模式       |  可读写  |

   

2. 小沃壁挂炉：

   |         参数名         |                      操作权限                      |
   | :--------------------: | :------------------------------------------------: |
   |         网关ID         |                        只读                        |
   |        壁挂炉ID        |                        只读                        |
   |     壁挂炉在线状态     |                        只读                        |
   |         开关机         |                       可读写                       |
   |        冬夏模式        |                       可读写                       |
   | 自动控制采暖水目标温度 |                       可读写                       |
   |   卫浴水短时预热开关   |    可读写（仅在壁挂炉支持卫浴水预热功能时开放）    |
   |     采暖水目标温度     | 自动控制采暖水目标温度功能禁止时可读写；允许时只读 |
   |     卫浴水目标温度     |                       可读写                       |
   |     采暖水出水温度     |                        只读                        |
   |     卫浴水出水温度     |                        只读                        |
   |         故障码         |                        只读                        |
   |        火焰状态        |                        只读                        |
   |         水压值         |                        只读                        |

   

3. 第三方壁挂炉：

   |     参数名     |               读写               |
   | :------------: | :------------------------------: |
   |     网关ID     |               只读               |
   |  网关在线状态  |               只读               |
   |    自动控制    |              可读写              |
   |    采暖允许    |              可读写              |
   |    卫浴允许    |              可读写              |
   | 采暖水目标温度 | 自动控制禁止时可读写；允许时只读 |
   | 卫浴水目标温度 |              可读写              |
   | 采暖水实际温度 |               只读               |
   | 卫浴水实际温度 |               只读               |
   |     故障码     |               只读               |

   