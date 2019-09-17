
给应用添加属性`android:persistent="true"`，并把应用放到 /system/app 下，重启系统，
1. 会开机启动该 app
2. 更新 versionCode，adb install -r，该应用的进程并不能重启

```xml
    <application
        android:persistent="true">
    </application>
```

3. adb install -r 后重启系统，该应用并没有启动
> 说明 `android:persistent="true"`这个属性只有第一个app版本才有效，覆盖安装后就没效了，并且设置了这个属性的应用 Android 推荐不要进行应用更新。





参考资料
* ![Android应用具有persistent属性时升级清理AMS缓存数据](https://www.icode9.com/content-4-189600.html)
* ![Android persistent机制](http://linqinan.com/2019/03/06/Android%20persistent%E6%9C%BA%E5%88%B6/) 
