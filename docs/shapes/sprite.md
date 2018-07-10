# Sprite (精灵)
继承于 H.Shapes.Element

## 构造方法

#### **constructor(options)**
- 参数
    - {Object} options
    - 属性列表
        
        | 名称         | 类型         | 默认值       | 描述        |
        |-------------|-------------|-------------|-------------|
        | status | `String` |  | 当前状态 |
        | defaultStatus | `String` |  | 默认状态，当某个状态结束时，会回到默认状态 |
        | statusData | `Object` | {} | 状态数据 |
    - options.statusData 数据结构
      ```js
        const statusData = {
          stand: {
            // 每一帧坐标数据
            0: {
              left: 0,
              top: 0
            },
            length: 1, // 动画总帧数
            width: 200, // 每一帧图像宽度
            height: 100, // 每一帧图像高度
            frameDelay: 100, // 每一帧延迟时间（单位毫秒）
            src: 'https://xxx.com/xxx.png', // 图像资源路径
            loopCount: 1 // 循环播放次数（无限循环播放设置空值即可）
          },

          walk: {
            0: {
              left: 0,
              top: 0
            },
            1: {
              left: 200,
              top: 0
            },
            2: {
              left: 400,
              top: 0
            },
            length: 3,
            width: 200,
            height: 100,
            frameDelay: 100,
            src: 'https://xxx.com/xxx.png',
            loopCount: 0
          },
          // status more ...
        };
      
      ```
- 示例

    ```js
      const sprite = new H.Shapes.Sprite({
        left: 100,
        top: 50,
        status: 'stand',
        defaultStatus: 'stand',
        statusData: {
          stand: {
            0: {
              left: 0,
              top: 0
            },
            length: 1, 
            width: 200,
            height: 100,
            frameDelay: 100,
            src: 'https://xxx.com/xxx.png',
            loopCount: 1
          },

          walk: {
            0: {
              left: 0,
              top: 0
            },
            1: {
              left: 200,
              top: 0
            },
            2: {
              left: 400,
              top: 0
            },
            length: 3,
            width: 200,
            height: 100,
            frameDelay: 100,
            src: 'https://xxx.com/xxx.png',
            loopCount: 0
          },
        }
      });

      // 改变精灵状态，即可实现动作切换
      sprite.status = 'walk';
    ```