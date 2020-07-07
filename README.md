# PatchMatchStereo
PatchMatchStereo双目立体匹配算法完整实现，代码规范，注释丰富且清晰，CSDN同步教学

<table>
    <tr>
        <td ><center><img src="https://github.com/ethan-li-coding/PatchMatchStereo/blob/master/Data/Cone/im2.png"></center></td>
        <td ><center><img src="https://github.com/ethan-li-coding/PatchMatchStereo/blob/master/Data/Cone/im6.png"></center></td>
        <td ><center><img src="https://github.com/ethan-li-coding/PatchMatchStereo/blob/master/doc/exp/res/cone-d.png"></center></td>
        <td ><center><img src="https://github.com/ethan-li-coding/PatchMatchStereo/blob/master/doc/exp/res/cone-c.png"></center></td>
    </tr>
    <tr>
        <td ><center><img src="https://github.com/ethan-li-coding/PatchMatchStereo/blob/master/Data/Reindeer/view1.png"></center></td>
        <td ><center><img src="https://github.com/ethan-li-coding/PatchMatchStereo/blob/master/Data/Reindeer/view5.png"></center></td>
        <td ><center><img src="https://github.com/ethan-li-coding/PatchMatchStereo/blob/master/doc/exp/res/reindeer-d.png"></center></td>
        <td ><center><img src="https://github.com/ethan-li-coding/PatchMatchStereo/blob/master/doc/exp/res/reindeer-c.png"></center></td>
    </tr>
    <tr>
        <td ><center><img src="https://github.com/ethan-li-coding/PatchMatchStereo/blob/master/Data/Piano/im0.png"></center></td>
        <td ><center><img src="https://github.com/ethan-li-coding/PatchMatchStereo/blob/master/Data/Piano/im1.png"></center></td>
        <td ><center><img src="https://github.com/ethan-li-coding/PatchMatchStereo/blob/master/doc/exp/res/piano-d.png"></center></td>
        <td ><center><img src="https://github.com/ethan-li-coding/PatchMatchStereo/blob/master/doc/exp/res/piano-c.png"></center></td>
    </tr>
<table>
  
# CSDN博客
[【码上教学】【立体匹配系列】经典PatchMatch: （1）框架](https://ethanli.blog.csdn.net/article/details/107192399)

# 环境
windows10 / visual studio 2015&2019

# 第三方库
opencv310
<br>
百度网盘连接：https://pan.baidu.com/s/1_WD-KdPyDBazEIim7NU3jA 
<br>
提取码：aab4
<br><br>
解压后放将名称为OpenCV的文件夹复制到到3rdparty文件夹下
<br><br>若运行时提示缺少opencv_310(d).dll，则在OpenCV文件夹里找到对应的dll文件复制到程序exe所在的目录即可（Opencv\dll\opencv_310(d).dll），带d为debug库，不带d为release库。
<br><br>
只在实验部分调用opencv库读取和显示图像，也可替换成其他图像库

# 算法引导
算法框架图
<div align=center>
<img src="https://github.com/ethan-li-coding/PatchMatchStereo/blob/master/doc/exp/%E7%AE%97%E6%B3%95%E6%A1%86%E6%9E%B6.png" width=80%>
</div>
<br/>代码框架图<br/>
<div align=center>
<img src="https://github.com/ethan-li-coding/PatchMatchStereo/blob/master/doc/exp/%E4%BB%A3%E7%A0%81%E6%A1%86%E6%9E%B6.png" width=60%>
</div>

## Github图片不显示的解决办法
修改hosts

C:\Windows\System32\drivers\etc\hosts

在文件末尾添加：

``` cpp
# GitHub Start 
192.30.253.112    github.com 
192.30.253.119    gist.github.com
151.101.184.133    assets-cdn.github.com
151.101.184.133    raw.githubusercontent.com
151.101.184.133    gist.githubusercontent.com
151.101.184.133    cloud.githubusercontent.com
151.101.184.133    camo.githubusercontent.com
151.101.184.133    avatars0.githubusercontent.com
151.101.184.133    avatars1.githubusercontent.com
151.101.184.133    avatars2.githubusercontent.com
151.101.184.133    avatars3.githubusercontent.com
151.101.184.133    avatars4.githubusercontent.com
151.101.184.133    avatars5.githubusercontent.com
151.101.184.133    avatars6.githubusercontent.com
151.101.184.133    avatars7.githubusercontent.com
151.101.184.133    avatars8.githubusercontent.com
 
 # GitHub End
```
