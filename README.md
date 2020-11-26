# CustomSwitch
在xml中配置
```
    <Switch
        android:id="@+id/iv_switch"
        app:layout_constraintLeft_toLeftOf="parent"
        app:layout_constraintRight_toRightOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintBottom_toBottomOf="parent"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:gravity="center_vertical"
        android:switchMinWidth="87dp"
        android:checked="false"
        android:thumb="@drawable/shape_switcher_thumb_bg"
        android:track="@drawable/switcher_track" />
```
开始配置文件
默认不选择（drawable文件下）switcher_bg_on.xml
```
<layer-list xmlns:android="http://schemas.android.com/apk/res/android"
    android:shape="rectangle">
    <item android:height="41dp" android:width="87dp">
        <bitmap android:src="@drawable/switcher_track_on" />
    </item>
</layer-list>
```
选中状态 switcher_bg_off.xml
```
<layer-list xmlns:android="http://schemas.android.com/apk/res/android"
    android:shape="rectangle">
    <item android:height="41dp" android:width="87dp" >
        <bitmap android:src="@drawable/switcher_track_off" />
    </item>
</layer-list>
```
切换时的左右滚动圆球可以上面设置文字（这里颜色设置透明） shape_switcher_thumb_bg.xml
```
<shape xmlns:android="http://schemas.android.com/apk/res/android"
    android:shape="rectangle">
    <corners android:radius="15.5dp" />
    <size android:width="41dp" android:height="41dp"/>
    <!-- 边框填充的颜色 -->
    <solid android:color="#0d2e65" />
    <stroke android:color="@android:color/transparent"
        android:width="8dp"/>
</shape>
```
开始设置左右切换选中 switcher_track.xml
```
<selector xmlns:android="http://schemas.android.com/apk/res/android"
    >
    <item android:state_checked="true" android:drawable="@drawable/switcher_bg_on" />
    <item  android:drawable="@drawable/switcher_bg_off" />
</selector>
```
关于Switch 设置文字配置属性
android:showText="true" ＜/br＞
android:switchTextAppearance="@style/switchtheme"＜/br＞
android:textOff="  关  "＜/br＞
android:textOn="   开  "





