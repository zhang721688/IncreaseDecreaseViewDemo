# IncreaseDecreaseViewDemo
数量增减变化的一个控件.

#### 效果图
![Image text](/image/view1.png)

![Image text](/image/view2.png)

![Image text](/image/view3.png)

#### 引入依赖
引入依赖:
```
implementation 'com.zxn.crease:CreaseViewLib:1.1.4'
```
    
#### 使用:
xml布局中放置控件1
```
<com.zxn.crease.CreaseView
    android:id="@+id/creaseview"
    android:layout_width="wrap_content"
    android:layout_height="30dp"
    app:decreaseIcon="@drawable/bg_d_sc_oval_times"
    app:increaseIcon="@drawable/bg_d_sc_oval_times"
    app:numBackground="@drawable/bg_d_sp_rec_r_times" />
```
xml布局中放置控件2
```
<com.zxn.crease.CreaseView
    android:id="@+id/cv2"
    app:numEditable="false"
    android:layout_width="wrap_content"
    android:layout_height="20dp"
    android:layout_marginTop="@dimen/dp_20"
    android:background="@color/c_ffffff"
    app:buttonTextColor="@color/sc_enabled_text_c_crease_view"
    app:numBackground="@drawable/bg_sp_rec_r4_c_e0e0e2" />
```
 属性使用:
 - decreaseIcon
     减少数量符号能否点击的背景选择器
 - increaseIcon
     增加数量符号能否点击的背景选择器
 - numBackground
     数字框的背景
 - buttonTextColor
     增加和减少符号的文字符号颜色,能否点击的颜色选择器.
 - numEditable
     控制是否可进行键盘输入的操作,默认为true,可进行键盘录入.
注意事项:
- 布局中需要制定具体的高度:
`android:layout_height="20dp"`
       
代码中的应用:
```
creaseview = (CreaseView) findViewById(R.id.creaseview);
creaseview.setMaxNum(10);
creaseview.setMinNum(1);
creaseview.setNum(1);
//输入值变化后的回调.
creaseview.setOnCreaseChangeListener(new CreaseView.OnCreaseChangeListener() {
    @Override
    public void onCreasedChanged(View view, int num) {
        //Toast.makeText(MainActivity.this, "num:" + num, Toast.LENGTH_SHORT).show();
        Log.i("MainActivity", "onCreasedChanged: -->"+num);
    }
});
```

#### 版本日志
v1.1.4:
- 增加属性`buttonTextEnabled`控制是否显示增减按钮文字,默认为true.

- 新增属性`unit`,控制是否显示单位,默认为空字符串.

- 新增属性`multiple`,控制按照指定倍数变化,默认为1.

- 解决了变化监听回调多次的bug.

#### 打标签:

数量增减控件1.1.2:配置高度属性
```
git tag -a v1.1.2 -m '配置高度属性'
git push origin v1.1.2
git tag
```

数量增减控件1.1.1:配置高度属性
```
git tag -a v1.1.1 -m '配置高度属性'
git push origin v1.1.1
git tag
```

数量增减控件1.1.0:键盘输入为空的时候,加减按钮逻辑处理
```
git tag -a v1.1.0 -m '键盘输入为空的时候,加减按钮逻辑处理'
git push origin v1.1.0
git tag
```

数量增减控件1.0.9:1,增加设置数字颜色属性,2,完善修复可驱动控件高度
```
git tag -a v1.0.9 -m '1,增加设置数字颜色属性,2,完善修复可驱动控件高度'
git push origin v1.0.9
git tag
```

数量增减控件1.0.8:1,增加数字输入框的点击事件;2,增加方法控制加减按钮是否可点击.
```
git tag -a v1.0.8 -m '1,增加数字输入框的点击事件;2,增加方法控制加减按钮是否可点击'
git push origin v1.0.8
git tag
```

数量增减控件1.0.7:代码中设置当前数量的方法,不进行点击回调.
```
git tag -a v1.0.7 -m '数量增减控件1.0.7:代码中设置当前数量的方法,不进行点击回调'
git push origin v1.0.7
git tag
```

数量增减控件1.0.6:完善.
```
git tag -a v1.0.6 -m '数量增减控件1.0.6:完善'
git push origin v1.0.6
git tag
```

数量增减控件1.0.5:完善.
```
git tag -a v1.0.5 -m '数量增减控件1.0.5:完善'
git push origin v1.0.5
git tag
```



数量增减控件1.0.4:1,增加设置加减符号文字颜色属性.2,增加控制是否可进行数字编辑属性	
```
git tag -a v1.0.4 -m '数量增减控件1.0.4:1,增加设置加减符号文字颜色属性.2,增加控制是否可进行数字编辑属性'
git push origin v1.0.4
git tag
```

数量增减控件1.0.3:增加方法判断输入框是否为空
```
git tag -a v1.0.3 -m '数量增减控件1.0.3:增加方法判断输入框是否为空'
git push origin v1.0.3
git tag
```
	




    
