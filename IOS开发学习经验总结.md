# IOS开发学习经验总结

## 关于Button设置圆角

- 可以通过代码直接设置

  ```swift
  //设置圆角（适应其他控件）
      loginBtn.layer.cornerRadius = 10.0f ;
  ```

  

- 也可以通过Xcode工具栏设置

  ```swift
  show the identity inspector -> User Definded Runtime Attributes
  在下面添加运行时属性：
  cornerRadius = 10.0f
  即可
  ```

  

## 关于设置view识图透明而子识图/控件不透明

- 在右侧菜单栏中设置

  ```
  Show the Attributes inspector -> background
  在下拉选单中选择Custom
  将背景图设置为透明即可。
  ```

  

## 关于设置应用程序打开时的默认StoryBoard

- 找到项目中的**info.plist**文件
- 依次展开**Application Scene Manifest** -> **Scene Configuration** -> **Application Session Role** -> **Defalut Configration** -> **Storyboard Name** 设置为**你想默认打开的Storyboard**



## UIView设置圆角

修改UIView中的属性。

```swift
UIView.layer.cornerRadius = 10
```



## UIScreen中的bounds和nativeBounds

bounds返回视图以自身为参考的坐标和视图自己的大小。

nativeBounds返回设备的屏幕尺寸。

```swift
let screenRec1 = UIScreen.main.bounds.self
let screenRec2 = UIScreen.main.nativeBounds.self

output:
(0.0, 0.0, 414.0, 736.0)
(0.0, 0.0, 1080.0, 1920.0)
```



## UIViewController的显示样式

这个困扰了很久的问题，终于找到答案了。

[简书上关于这个的一篇文章](https://www.jianshu.com/p/af990d83815e)

在UIViewController这个类中，有一个modalPresentationStyle属性，这个属性是用来设置视图显示的样式的。

```swift
VC.modalPresentationStyle = UIModalPresentationStyle.formSheet //设置全屏显示

//UIModalPresentationStyle的declaration
enum UIModalPresentationStyle : Int

Presentations
case automatic
The default presentation style chosen by the system.
case none
A presentation style that indicates no adaptations should be made.

case fullScreen
A presentation style in which the presented view covers the screen.

case pageSheet
A presentation style that partially covers the underlying content.

case formSheet
A presentation style that displays the content centered in the screen.

case currentContext
A presentation style where the content is displayed over another view controller’s content.

case custom
A custom view presentation style that is managed by a custom presentation controller and one or more custom animator objects.

case overFullScreen
A view presentation style in which the presented view covers the screen.

case overCurrentContext
A presentation style where the content is displayed over another view controller’s content.

case popover
A presentation style where the content is displayed in a popover view.

case blurOverFullScreen
A presentation style that blurs the underlying content before displaying new content in a full-screen presentation.

```





## view中的cliptoBounds属性

设置是否裁剪子视图中超出父视图的部分。默认为NO。

[文章](https://www.jianshu.com/p/1f94bed28b93)



## NavigationBar相关属性的设置

不能在navigationController本身设置，要在它的栈视图中设置。

比如这个设置标题

```swift
let vc1 = UIViewController()
vc1.title = "This is title"
vc1.view.backgroundColor = UIColor.brown
self.pushViewController(vc1, animated: true)
```

这样设置就不行

```swift
class LogInSwitchingViewController: UINavigationController {

    override func viewDidLoad() {
        super.viewDidLoad()
        // Do any additional setup after loading the view.
        self.view.backgroundColor = UIColor.white

        self.navigationItem.title = "This is title"
        self.navigationBar.tintColor = UIColor.black

        let vc1 = UIViewController()
        vc1.view.backgroundColor = UIColor.brown
        self.pushViewController(vc1, animated: true)
    }
```



## NavigationController的坑

NavigationController只是一个容器，至少要有一个子视图才能正常工作。





## 显示和关闭一个视图

```swift
self.dismiss(animated: true, completion: nil)、

func present(_ viewControllerToPresent: UIViewController, animated flag: Bool, completion: (() -> Void)? = nil)
```





## 设置textfield字符边距的两种办法

由于一开始不会设置输入框style，导致输入的字符总是紧贴着边框的。

以下方法可以解决这个问题

```
textField?.setValue(NSNumber(value: 10), forKey: "paddingLeft")
//设置textField左边距10
//还有paddingTop, paddingBottom, paddingRight

textField.leftViewMode = UITextField.ViewMode.always
textField.leftView = UIView(frame: CGRect(x: 0,y: 0,width: 8,height: 0))
textField.leftViewMode = UITextField.ViewMode.always

//设置左边距8
```

设置了默认边框样式以后字符就不会紧贴边框了，这个方法也用不到了。

不过可以用来在输入框的左边添加图片。





## 设置textfield输入框的两种方法

```
//默认边框，推荐采用这种方法。
pwdField.borderStyle = .roundedRect

//自定义边框
nameField.layer.borderWidth = CGFloat(0.5)
nameField.layer.borderColor = UIColor.gray.cgColor
nameField.layer.cornerRadius = 5
```



## 弹出和设置警告窗口

```swift
let alert = UIAlertController(title: "第三方登录", message: nil, preferredStyle: .actionSheet)
alert.addAction(UIAlertAction(title: "QQ登录", style: .default, handler: nil))
alert.addAction(UIAlertAction(title: "手机号登录", style: .destructive, handler: nil))
alert.addAction(UIAlertAction(title: "取消", style: .cancel, handler: nil))
present(alert, animated: true, completion: nil)
```



## 关于标签一些属性的设置

```swift
//文本
labl.text = "用户登录"
//对齐方式
labl.textAlignment = NSTextAlignment.center
//字体大小
labl.font = UIFont.systemFont(ofSize: 36)

```



## 关于输入框一些属性的设置

```swift
pwdField.borderStyle = .roundedRect
//pwdField.layer.borderWidth = CGFloat(0.5)
//pwdField.layer.borderColor = UIColor.gray.cgColor
pwdField.returnKeyType = UIReturnKeyType.done
pwdField.leftViewMode = UITextField.ViewMode.always
//pwdField.leftView = UIView(frame: CGRect(x: 0, y: 0, width: 8, height: 0))
pwdField.isSecureTextEntry = true
pwdField.placeholder = "Password"
```



## 设置返回键类型以及收起键盘

```swift
//设置返回键类型
nameField.returnKeyType = UIReturnKeyType.done

//设置done收起键盘
nameField.addTarget(self, action: #selector(endEdit), for: .editingDidEndOnExit)
pwdField.addTarget(self, action: #selector(endEdit), for: .editingDidEndOnExit)
        
@objc func endEdit(){
        nameField.resignFirstResponder()
        pwdField.resignFirstResponder()
    }
```

