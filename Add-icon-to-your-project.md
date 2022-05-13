# 如何向你的项目添加程序图标？
## renpy.org中文档的原文（如果不会或看不懂或不想看，可以直奔主题前往下方翻译与案例代码）
### [Special Files](https://renpy.org/doc/html/build.html#special-files)
There are two files that can be included in your game's base directory to customize the build.

#### icon.ico
The icon that is used on Windows.
#### icon.icns
The icon that is used on Macintosh.  
These icon files must be in specific formats. You'll need to use a program or web service (such as https://anyconv.com/png-to-ico-converter/ and https://anyconv.com/png-to-icns-converter/ ) to convert them.

### [Icon and Presplash Image](https://renpy.org/doc/html/android.html#icon-and-presplash-images)
#### Icon
Ren'Py will create an icon from your app from two files in the game's base directory:

##### android-icon_foreground.png
The foreground layer of the icon. This should be 432x432 pixels and transparent.
##### android-icon_background.png
The background layer of the icon. This should be 432x432 pixels and opaque.
Android adaptive icons work by masking the two layers of the icon to an area that is at least 132x132 pixels, in the center. The area outside of this safe space may be shown, but it might be masked out, too. Bleeding outside of the safe area is encouraged. The two layers might move a little relative to each other when the icon is dragged around.

For more information about adaptive icons, please check out:

https://medium.com/google-design/designing-adaptive-icons-515af294c783  
Note that 1dp corresponds to 4 actual pixels.

When generating the application, Ren'Py will convert these files to an appropriate size for each device, and will generate static icons for devices that do not support adaptive icons.

## 翻译：
### [特殊的文件](https://www.renpy.cn/doc/build.html#special-files)
有两个可被包含在游戏根目录下的文件可以自定义你的构建。

#### icon.ico
这个图标被用于Windows
#### icon.icns
这个图标被用于Macintosh。  
这些图标均需要采用特定的格式。你需要使用某些程序或互联网服务（如 https://anyconv.com/png-to-ico-converter/ 或 https://anyconv.com/png-to-icns-converter/） 来转换它们。

译者注：你还可以使用'ffmpeg -i input.png output.ico'来进行转换。

### [Icon and Presplash Image](https://renpy.org/doc/html/android.html#icon-and-presplash-images)
#### Icon
Ren’Py使用游戏根目录中的两个图片文件生成app图标：

##### android-icon_foreground.png
图片的前景层。它应该是432px*432px大小且具有透明度。
##### android-icon_background.png
图片的背景层。它应该是432px*432px大小且完全不透明.
安卓的自适应图标机制是这样工作的，将两个图标放在至少132×132像素的区域中并中央对齐，然后将前景层盖在背景层上。 有可能在这个区域之外的图像也会显示，但也可能会被遮挡住。最好在安全区域之外还预留一些出血位(bleeding)。 当拖拽图标时，两个图层可能会保持相对位置有一点移动。

想获取有关动态图标的更多内容，请访问：

https://medium.com/google-design/designing-adaptive-icons-515af294c783  
请注意屏幕上的1dp会对应4px实际像素。。

生成应用时，Ren'Py会把这些文件转换为适合不同设备的尺寸，并会为不支持动态图标的设备生成静态的图标。

## 让我们来看一个案例
![样例图片，项目为自带的TheQuestion](/_images/addicons.png "Ren'Py的案例项目--The Question")
