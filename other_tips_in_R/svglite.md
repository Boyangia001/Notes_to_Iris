# 在RStudio中实现用svglite包将图片插入ppt并svg化图片：

## 1.安装tidyverse系列包，特别是其中的svglite包。在RStudio console 中运行：
```r
install.packages("tidyverse")
install.packages("svglite")
```
加载所需的库：
```r
library(tidyverse)
library(svglite)
```
准备你的数据和绘图代码。假设你已经有了绘制图形的R代码。  
使用svglite包将图形保存为SVG格式。例如：
```r
svglite("your_plot.svg", width = 10, height = 8)
# 这里放置你的绘图代码
dev.off()
```
生成的SVG文件可以直接导入到PowerPoint中。在PowerPoint中，你可以通过"插入" > "图片" > "此设备中的图片"来插入SVG文件。
在PowerPoint中，你可以对SVG图片进行编辑，包括调整每个绘图元素和文本。
### 注意事项：

SVG格式允许你在PowerPoint中直接编辑图形的各个元素。  
文字会被识别为文本框，方便进行文字调整。  
这种方法比之前使用PDF然后在Adobe Illustrator或Inkscape中进行矢量化操作更加便捷。  
