# Android-Jackpack-Note

## 甚麼是Jackpack
Jetpack 是一個集合函式庫、工具、架構的一個組合，讓開發 App 更為快速。

![](http://bp.googleblog.cn/-dwL58chu7wo/WvD1RrHln3I/AAAAAAAAFUg/cRTc0IZga_wMPTWr3CI53IZ5BwtnZMeYACLcBGAs/s1600/Screen%2BShot%2B2018-05-05%2Bat%2B11.49.30%2BAMimage1.png)

## 優點
 - 依據開發需求可以分開組件用
 - 任何版本平台都可以執行
 - 程式碼更為簡潔、穩定

## 新組件
 - WorkManager alpha 版
 - Navigation alpha 版
 - Pagging 穩定版
 - Slices  alpha 版
 - Android KTX alpha 版

## Android KTX
是一個 Kotlin 擴充的 Lib，用途為簡化程式碼。
[文件](https://developer.android.google.cn/kotlin/ktx#kotlin)

原始
```kotlin
view.viewTreeObserver.addOnPreDrawListener(
  object : ViewTreeObserver.OnPreDrawListener {
    override fun onPreDraw(): Boolean {
      viewTreeObserver.removeOnPreDrawListener(this)
      actionToBeTriggered()
      return true
    }
});
```
使用過 Android KTX
```kotlin
view.doOnPreDraw { actionToBeTriggered() }
```
## Slices
Slices 是以搜尋的方式顯示，讓使用者不須搜尋後開網頁找，而是搜尋時直接多出結果的選單。
[文件](https://developer.android.com/guide/slices/)
![](http://bp.googleblog.cn/-CtLmyY1io2Y/WvD5YMU_H2I/AAAAAAAAFVE/JBEtgrYvviU4rXWhs2niHzCYhbZfH66rQCLcBGAs/s1600/Screen%2BShot%2B2018-05-07%2Bat%2B6.10.13%2BPM.png)

## Paging
輕鬆加載和呈現大型數據集，同時在您的 RecyclerView 中進行快速、無限滾動。

## 參考連結
> http://developers.googleblog.cn/2018/05/android-jetpack.html
