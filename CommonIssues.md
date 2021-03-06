< [Back](README.md)

常见问题强调
========

201303
-----
* 视图必须正确设置 `autoresizingMask`。

* 把一个 viewController 的 view 加入到另一个 viewController 的 view 时，必须用 `addChildViewController:` 方法把这两个 viewController 关联起来。

* 给界面贴图一定要保证图片比例正确，避免拉伸失真。举例给按钮设置背景，图片的大小跟按钮的一致吗？不一致是不是要设置拉伸啊。@2x的图贴了吗？

* 永远不要用 `CGRectMake(10, 10, 300, 200)` 这样的方式设置视图尺寸。如果你不得不强制设置视图位置的话，应该依靠现有视图和常量进行计算。比如：

```Objective-C
CGFloat margin = 10.f;
CGRect bounds = superView.bounds;
CGFloat toolbarHeight = toolbar.frame.size.height;
view.frame = CGRect(margin, margin, bounds.size.width - margin*2, bounds.size.height - margin*2 - toolbarHeight);
```

* 除非涉及 `UIWindow` 否则永远不要用 `UIScreen` 的尺寸。99%的情况都应参照父视图的尺寸。

* 任务下发后有问题及时沟通，缺啥要啥，不清楚及时沟通，别等人来问你时才说。

* 错误发生先看错误信息，错误是什么都没搞清就别问其他人了。

* 如果一个任务你确定完不成了，赶快求助，别怕丢人。光憋在那里也提高不了，凭白浪费生命。没人笑话你（就算有那你也得给自己提高的机会吧）。
