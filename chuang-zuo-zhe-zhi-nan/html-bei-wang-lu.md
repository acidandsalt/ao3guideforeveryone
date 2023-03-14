---
description: AO3只支持有限的几种HTML。
---

# HTML备忘录

### 一些常用HTML

* **标题：**`h1, h2, h3, h4, h5, h6`
  * \<h1>大标题\</h1>
  * \<h2>副标题\</h2>
  * \<h3>章标题\</h3>
  * \<h4>幕标题\</h4>
  * \<h5>小标题\</h5>
  * \<h6>脚注标题\</h6>
* **斜体与加粗：**`em, strong`
  * 斜体：\<em>_Rodney_\</em> McKay
  * 加粗：I will \<strong>**never**\</strong> understand you!
* **引用：**`blockquote, q, cite`
  *   \<blockquote>

      > 段落引用

      \</blockquote>
  * \<q>词语引用\</q>
  * \<cite>外国文字、语句或标题引用\</cite>
* **超链接：**\<a href="这里放链接地址">这里写文字\</a>

想了解更多HTML的用法，可以参考一些HTML指导文档，比如：[https://developer.mozilla.org/zh-CN/docs/Web/HTML](https://developer.mozilla.org/zh-CN/docs/Web/HTML)

### AO3自动修正HTML

在HTML模式下编辑发布作品时，AO3会自动修正一些HTML格式。

* 如果两个段落之间有空行，自动增添分段标记（\<p>\</p>）
* 如果在两行文本之间有一个回车，自动增添换行标记（\</br>）
* 如果连续写入两个换行标记（\<br />\<br />），自动变换为分段标记
* 如果段落之间出现两个连续空行，自动增加段落间空白的长度（用\<p>\&nbsp;\</p>）
* 如果标记的嵌套顺序错误（比如\<em>\<strong>_**text!**_\</em>\</strong>），自动修正顺序（变成\<em>\<strong>_**text!**_\</strong>\</em>）
* 如果忘记写入标记的右半边（带“/”的那半边），自动在段落结尾加入（假如你想斜体一个词，结果忘了打\</em>，这个词往后的一整段都会自动斜体）
* 如果隔了几段才写入标记右半边（整个标记中包含了几个段落），自动调整为每个段落单独用标记括起（标准写法）
* 如果你使用了自定义HTML（比如用\<ul>插入无序列表）又不想分行分段，那你只能统统写在同一行里，要不然就会自动被插入\</br>或\</p>
* 如果你的某一段文本看起来比其他的大一点，那可能是格式处理器没在这段文字前后加分段标记，请手动修正

### AO3支持的HTML

`a, abbr, acronym, address, [align], [alt], [axis], b, big, blockquote, br, caption, center, cite, [class], code, col, colgroup, dd, del, dfn, div, dl, dt, em, figcaption, figure, h1, h2, h3, h4, h5, h6, [height], hr, [href], i, img, ins, kbd, li, [name], ol, p, pre, q, s, samp, small, span, [src], strike, strong, sub, sup, table, tbody, td, tfoot, th, thead, [title], tr, tt, u, ul, var, [width]`



【注】本篇资料来自AO3的HTML帮助文档：[https://archiveofourown.org/help/html-help.html](https://archiveofourown.org/help/html-help.html)
