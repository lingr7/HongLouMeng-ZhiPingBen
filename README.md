<!--
 * @Author: your name
 * @Date: 2020-04-24 15:31:30
 * @LastEditTime: 2020-04-27 14:49:29
 * @LastEditors: your name
 * @Description: In User Settings Edit
 * @FilePath: \HongLouMeng-ZhiPingBen\README.md
 -->

# HongLouMeng ZhiPingBen

最初的预览目标版本

[拙编《红楼梦脂评汇校本》出版，发布定稿电子版----------_kolistan_新浪博客 ](http://blog.sina.com.cn/s/blog_5057dca80101es12.html)

然后是亚马逊

[《红楼梦脂评汇校本 (BookDNA典藏书系)》 曹雪芹, 脂砚斋, 吴铭恩 书评 简介 电子书下载 Kindle电子书](  https://www.amazon.cn/dp/B00M2R1RKQ?t=hwg_ca_fx_7-23&tag=hwg_ca_fx_7-23)

接着我拿到了epub格式，接着就是一波转换。

然后有了中间文件，重绘了批注图。最初实现基本功能能看的版本只花了2天时间就做出来了。

## 从码云回归

曾经迁移至：https://gitee.com/lingr7/The-Story-of-the-Stone/

推荐：上译厂刘风，张国立 红楼梦有声书 https://www.ximalaya.com/renwenjp/20654769/ 最初的预览目标版本

## 编译方法

推荐使用TeXLive 2022
可从清华开源镜像网站获取安装包。
windows下，使用 ./tex_src/book/make.bat，自动编译，生成stone.pdf文件。编译方法参考了https://github.com/CTeX-org/lshort-zh-cn

## 2020年变化

感谢：[关于多行标题居中悬挂对齐在目录中的换行问题 · Issue #111 · CTeX-org/forum]( https://github.com/CTeX-org/forum/issues/111) 

```latex
\usepackage{varwidth} %% 提供 varwidth 环境

\usepackage[titles]{tocloft}
\setlength{\cftchapnumwidth}{8\ccwd}

\ctexset{
    chapter = {
        format += \centering,
        name = {第,回},
        nameformat += \chapternameformat,
        titleformat = \chaptertitleformat
    }
}
\newcommand{\chapternameformat}[1]{\kaishu #1}
\newcommand{\chaptertitleformat}[1]{%
    \CTEXifname{\parbox[t]{8\ccwd}{#1}}{#1}}
```

## 2021年变化

生僻字相关，设置fontset=windows以支持一些生僻字；
移除了自己的100+条笔记；
增加了带圈数字支持；
修改了圆形和菱形及方形；
修正引号使用；
尝试了章节尾注，把全部尾注替换为脚注暂时未做；

## 2022年变化

编译stone.tex，使用lshort-zh-cn.pdf同款样式。
每章脚注。19 61 67 80有章节标题脚注，放在第一行。

## 截图展示

见[项目码云wiki](https://gitee.com/lingr7/The-Story-of-the-Stone/wikis/Home)

## Todo

- [ ] 诗句

- [ ] 对联
