# flutter_dialog

### 参数说明
|属性|说明|类型|默认值
|---|---|---|---
|title|弹窗标题|String|-
|content|弹窗内容|String|-
|confirmContent|自定义按钮文本|String|-
|confirmTextColor|确定按钮文本颜色|Color|0xDD000000
|isCancel|是否有取消按钮，true：有 false：没有|bool|true
|confirmColor|确定按钮颜色|Color|0xFFFFFFFF
|cancelColor|取消按钮颜色|Color|0xFFFFFFFF
|outsideDismiss|点击弹窗外部关闭弹窗，true：可以关闭 false：不可关闭|bool|true
|confirmCallback|点击确定按钮回调|Function|-
|dismissCallback|弹窗关闭回调|Function|-

### 用法

#### 带有标题的Dialog
```Dart
 showDialog(
   context: context,
   barrierDismissible: false,
   builder: (_) {
     return CustomDialog(
       title: '这是一个标题',
       content: '这里是弹窗的提示内容',
     );
   }
 );
```
#### 自定义确定按钮颜色
```Dart
showDialog(
  context: context,
  barrierDismissible: false,
  builder: (_) {
    return CustomDialog(
      title: '这是一个标题',
      content: '这里是弹窗的提示内容',
      isCancel: true,
      confirmColor: Colors.green[400]
    );
  }
);
```
#### Dialog按钮点击回调监听
```Dart
showDialog(
  context: context,
  barrierDismissible: false,
  builder: (_) {
    return CustomDialog(
      title: '这是一个标题',
      content: '这里是弹窗的提示内容',
      confirmCallback: () {
        print('-----------点击了确定按钮');
      },
    );
  }
);
```
更多用例请查看项目中MyHomePage.dart文件。

### 部分效果图

![img](./show/f1.png)

![img](./show/f2.png)

![img](./show/f3.png)

![img](./show/f4.png)

![img](./show/f5.png)

![img](./show/f6.png)
