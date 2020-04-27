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

接着我拿到了epub格式，接着就是一波转换

然后有了中间文件，重绘了批注图。

接下来是做笔记的方法

[新样式 ElegantPar 发布-LaTeX工作室](http://www.latexstudio.net/archives/2528)

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



![目录](https://picture-1258475985.cos.ap-chengdu.myqcloud.com/imgimage-20200427142625952.png)


![第六回](https://picture-1258475985.cos.ap-chengdu.myqcloud.com/img20200427143158.png)

## Todo
- [ ] 诗句

- [ ] 对联

- [ ] 脚注
