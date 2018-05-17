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
[文件](https://developer.android.com/topic/libraries/architecture/paging/)

[範例](https://blog.csdn.net/zhangphil/article/details/78627332)

## Navigation

儘管Activity是系統提供的應用界面的入口點，但在相互分享數據以及轉場方面，Activity表現得不夠靈活。

重點是讓單Activity應用成為首選架構。利用 Navigation 對Fragment的原生支持，您可以獲得架構組件的所有好處（例如生命週期和ViewModel），

同時讓此組件為您處理FragmentTransaction的複雜性。此外，導航組件還可以讓您聲明我們為您處理的轉場。

它可以自動構建正確的“向上”和“返回”行為，包含對深層鏈接的完整支持，

並提供了幫助程序，用於將導航關聯到合適的UI小部件，

例如抽屜式導航欄和底部導航。但這些並不是全部！Android Studio 3.2中的導航編輯器讓您可以直觀地查看和管理導航屬性：

![](http://bp.googleblog.cn/-GKJGCirclDI/WvD1qlznfAI/AAAAAAAAFUo/zaTtY_hbSegdNssiTKqt0RvmarnRgUZrQCLcBGAs/s1600/pasted%2Bimage%2B0%2B%25282%2529image2.png)
[Video](https://www.youtube.com/watch?v=8GCXtCjtg40)

## WorkManager
執行某個任務可能因為外在因素可能被中斷，以前的解決方案有 Job scheduler (os5以上)、Firebase Job Dispatcher(os5以下)、Alarms Manager
WorkManager 提供了一種簡化的方案。
[範例](https://android.jlelse.eu/exploring-jetpack-the-power-of-chains-in-the-workmanager-apis-30509ca4b2c)

## 參考連結
> http://developers.googleblog.cn/2018/05/android-jetpack.html
