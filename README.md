>-----------------------------------------------------------------------
>
>* @Author  : Jun Xuan (idxuan@hotmail.com)
>* @Link    : http://idxuan.github.io
>* @Date    : 2014-05-01
>* @Version : 0.1.1
>* @Desc    : Vim 字典输入
>         插件编码参考源自[vimim-wubi](http://code.google.com/p/vimim-wubi)
>
>-----------------------------------------------------------------------

# Vim 字典输入

## 插件说明

吐槽一下，Vim 对非字母输入的用户来说太糟心了，让行云流水的输入变得磕磕碰碰的异常难受。曾经停用了两次 Vim 的使用，又舍不得捡了回来，输入法是停用最大的原因，很有些鸡肋的感觉。就算你的英文好也麻烦的很，总不能你写的都是代码和英文文档吧。不管如何，在我的周围里需要使用中文的机会太多了……

受到 VimIM 和 VimIM-wubi 的启发，最近在码能在 Vim 里使用的输入法，直接用 `vim-script` 编写。我是用“小鹤双拼输入法”的，VimIM 太麻烦，什么云输入之类的不适合我，作者又很长时间不更新了，有些小 BUG 因为功能太繁杂修改起来也较麻烦，想着干脆自己改造个适合自己的，哈哈，自己动手，丰衣足食嘛。以字词输入为重点，类似五笔输入，不考虑联想，用字典方式为主体架构。简单来说，就是输入字母，查找字典输出，输出什么都可以自己定义。

如果有同样需求的可以试用，欢迎多提宝贵意见哈：）

## 插件安装

* 使用插件管理器（Vundle）：增加配置语句 `Plugin 'idxuan/bx_vimim_dict'`；
* 手工下载：[Github](https://github.com/idxuan/bx_vimim_dict) 。点击右下角 `Download ZIP`，解压后把 `bx_vimim_dict.vim` 和字典文件 `bx_vimim_*.txt` 放到 Vim 的 `plugin` 目录下即可；
* 插件是中文输入插件，使用 `UTF-8`。所以 Vim 必须使用支持中文的编码，同时更改字典文件为相同编码。

## 使用说明

* 中英文输入切换：插入模式下使用 `CTRL-L`；
* 中英文标点切换：插入模式下使用 `CTRL-\`；
* 空格输入中文，回车输入原英文字母；
* 最多四键输入，`Ctrl+N、Ctrl+P` 上下选择中文；
* 默认使用小鹤双拼，如果需要使用五笔，请设置 `let g:bx_im_wubi_used=1`；
* 程序自带的是小鹤双拼和五笔码表，你也可以改成自己习惯的码表，只要按照 [a~z] 的顺序排列好，同时设置 g:bx_im_charfirst=字母 [a~z] 在码表文件中的开始行号即可。例如 `let g:bx_im_charfirst=[1,234,...]`。

## 更新历史

2014-04-24：

* 程序已初步调试完成，进入试用阶段。

## 修改

2017-10-06:

* 模拟 飞扬小鹤 中分号键上屏次选项的行为