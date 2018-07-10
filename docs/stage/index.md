# Stage (舞台)

## 构造方法

#### **constructor(options)**

- 参数
    - {Object} options
    - 属性列表
        
        | 名称         | 类型         | 默认值       | 描述        |
        |-------------|-------------|-------------|-------------|
        | domSelector | `String` | | 指定需要初始化的容器（匹配指定选择器的第一个元素） |
        | width | `Number` | 300 | 舞台宽度 |
        | height | `Number` | 150 | 舞台高度 |
        | openEventListener | `Boolean` | false | 是否开启事件监听 |

- 示例

    ```html
      <div id="my-canvas"></div>
    ```
    ```js
      const stage = new H.Stage({
        domSelector: '#my-canvas',
        width: 1800,
        height: 700,
        openEventListener: true,
      });
    ```

<br/>

## 属性

#### **bus** 
舞台事件总线

- 示例

    ```js
      const eventTypes = H.Utils.EventTypes;
      stage.bus
        .on(eventTypes.ELEMENT_MOUSE_ENTER, function ({e, target}) {
          console.log('element mouse enter', e, target);
        })
        .on(eventTypes.ELEMENT_MOUSE_LEAVE, function ({e, target}) {
          console.log('element mouse leave', e, target);
        });
    ```

<br/>

## 方法

#### **add(element1, element2, [...])**
添加元素到舞台

- 参数
  - ...element

    | 名称         | 类型         | 默认值       | 描述        |
    |-------------|-------------|-------------|-------------|
    | element | `Object` | null | 需要添加至舞台的元素（H.Shapes.Element实例） |
    
- 示例

    ```js
      const element1 = new H.Shapes.Element();
      const element2 = new H.Shapes.Element();
      stage.add(element1, element2);
    ```    

#### **remove(elementId)**
从舞台移除指定id的元素

- 参数
  - elementId

    | 名称         | 类型         | 默认值       | 描述        |
    |-------------|-------------|-------------|-------------|
    | elementId | `String` | - | 元素的id |
    
- 示例

    ```js
      stage.remove('1');
    ```

#### **getElementById(elementId)**
获取舞台上指定id的元素

- 参数
  - elementId

    | 名称         | 类型         | 默认值       | 描述        |
    |-------------|-------------|-------------|-------------|
    | elementId | `String` | - | 元素的id |

- 示例

    ```js
      const element = stage.getElementById('8');
    ```
