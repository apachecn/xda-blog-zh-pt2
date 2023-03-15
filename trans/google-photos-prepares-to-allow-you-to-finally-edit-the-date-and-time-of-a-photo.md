# Google 相册准备允许编辑照片的日期和时间

> 原文：<https://www.xda-developers.com/google-photos-prepares-to-allow-you-to-finally-edit-the-date-and-time-of-a-photo/>

谷歌照片一直是谷歌比较有用的服务之一。照片备份服务因其无限制、免费的备份功能以及强大的共享功能而广受好评。但谷歌照片一直落后的一个领域是编辑照片的能力。幸运的是，随着时间的推移，谷歌已经推出了越来越多的功能，允许你根据自己的喜好定制图片(尽管编辑功能不如一些竞争对手的强大)。

编辑您的照片以产生更好的图像是一回事，但是如何编辑您的图像以使其更容易组织呢？不幸的是，Google 相册修改 EXIF 数据的能力非常有限。即使在今天，编辑照片的日期和时间戳等基本内容的能力也仅限于桌面版。如果你主要在手机上管理你的照片(这样做并不可耻，Android 应用程序设计得非常好)，并且你想根据自己的喜好重新排列某些照片，这可能会令人沮丧。但是随着谷歌照片 2.7 版本的推出，这种情况可能会很快改变。APK 的拆除显示谷歌可能**很快会允许你编辑你照片的 EXIF 时间戳**。

虽然拆卸可以提供关于即将到来的特性的有价值的信息，但是这些特性完全有可能不会进入最终产品。不要把这些拆除作为一个新特性将被添加的证据，而是作为一个什么可能到来的暗示。

* * *

## Google 相册拆卸

在最新版本的 Google 相册中，APK 中有一个有趣的字符串，暗示了编辑照片时间戳的能力:

```
 <string name="photos_mediadetails_details_edit_datetime_icon_content_description">Edit icon to allow the user to edit the date/time of the media.</string> 
```

正如你所看到的，在图片细节屏幕中会有一个图标，允许你简单地编辑媒体的日期/时间。以前，您只能编辑位置 EXIF 数据。现在看来，更改日期和时间也将很快成为可能。这一新功能的进一步证据还可以在 APK 中添加的名为 **exif_datetime_item.xml** 的新布局文件中找到:

### Google 相册拆卸

**exif_datetime_item.xml**

```
 <?xml version="1.0" encoding="utf-8"?>
<LinearLayout android:orientation="horizontal" android: android:padding="@dimen/photos_mediadetails_item_padding" android:layout_width="fill_parent" android:layout_height="wrap_content" android:minHeight="@dimen/photos_mediadetails_item_min_height"
xmlns:andro>
<ImageView android:layout_gravity="center" android: android:padding="@dimen/photos_mediadetails_item_padding" android:layout_width="66.0dip" android:layout_height="36.0dip" />
<LinearLayout android:orientation="vertical" android:padding="@dimen/photos_mediadetails_item_padding" android:layout_width="0.0dip" android:layout_height="wrap_content" android:minHeight="@dimen/photos_mediadetails_item_min_height" android:layout_weight="1.0">
<TextView android:layout_gravity="start|center" android: android:paddingLeft="2.0dip" android:paddingTop="8.0dip" android:paddingRight="2.0dip" android:layout_width="fill_parent" android:layout_height="wrap_content" style="@style/quantum_text_subhead_black" />
<TextView android:textColor="@color/quantum_black_secondary_text" android:layout_gravity="start|center" android: android:paddingLeft="2.0dip" android:paddingRight="2.0dip" android:paddingBottom="8.0dip" android:layout_width="fill_parent" android:layout_height="wrap_content" style="@style/quantum_text_subhead_black" />
</LinearLayout>
<ImageView android:layout_gravity="center" android: android:padding="@dimen/photos_mediadetails_item_padding" android:visibility="gone" android:layout_width="66.0dip" android:layout_height="36.0dip" android:src="@drawable/quantum_ic_mode_edit_black_18" android:contentDescription="@string/photos_mediadetails_details_edit_datetime_icon_content_description" android:alpha="0.38" />
</LinearLayout> 
```

布局文件的名称和字符串的描述非常清楚:编辑照片的 EXIF 时间戳可能很快就会在 Android 版本的应用程序中提供。此外，这个布局文件似乎直接对应于添加的字符串，正如您可以看到它调用绘制“编辑图标”的位置。桌面用户(甚至 iOS 用户)拥有这种能力已经有一段时间了，所以希望它最终也能进入 Android。