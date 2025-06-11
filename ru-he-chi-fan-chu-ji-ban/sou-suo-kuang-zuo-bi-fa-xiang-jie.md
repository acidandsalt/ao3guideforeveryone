---
description: >-
  经常使用搜索框的小伙伴或许会发现，在点击搜索框但还未输入时，底下偶尔会出现一个标注着「tips」的提示框。这个东西叫做Hidden search
  operators——内嵌搜索运算符。这些运算符并未在界面上明示，但输入之后即可量身定制搜索结果。
---

# ※搜索框作弊法详解

AO3有三个搜索框可以使用内嵌搜索运算符：

* [筛选功能](ji-ben-sou-suo-fang-fa-search/shai-xuan-gong-neng-filter.md)中的`Search within results`栏
* [作品搜索页](ji-ben-sou-suo-fang-fa-search/ru-he-cha-zhao-zuo-pin-works.md)中的`Any Field`栏
* 网页顶部的搜索框

一个完整的搜索输入由三部分组成：「关键词」、「限定条件」和「排序依据」。其中「关键词」需要用<mark style="color:orange;">AND</mark>连接，而后两种只需要用空格分开。



### 关键词（Text Searches）

_——简单来讲就是大家搜索东西时本能敲上去的东西。_

AO3在处理搜索词的时候有这样一个特性：关键词只会**一起出现在搜索结果的同一个模块**中。（标题、标签、正文、附注都属于不同的模块。）

例子：假如你搜索「<mark style="color:green;">BTS 喜欢</mark>」，那么你的搜索结果中会出现附注中有「<mark style="color:green;">我喜欢BTS！</mark>」的作品，而**不会有**标题中包含「<mark style="color:green;">喜欢</mark>」、标签中包含「<mark style="color:green;">BTS</mark>」的文章。

**因此，如果你需要搜索可能处在不同模块的关键词，用`AND`连接它们！**

比如：我想搜索包含「BTS」、「狗狗」和「慢热」的作品，它们可能处于不同的模块

那么我应该在搜索框中输入`BTS AND puppies AND "slow burn"`

_PS. 英文双引号""的作用是精确搜索，意思是搜索结果中只会包含slow burn这个词组，两个词不会分开也不会颠倒顺序。_



### 限定条件（Work Properties）

_——顾名思义，用来限定想看什么样的文章的。_

AO3提供的参考里有很多筛

选条件，用处较多的罗列如下，比较冷门的在折叠栏内，感兴趣的朋友请点开查看。

{% hint style="danger" %}
<mark style="color:red;">**注意：这里使用的标点符号均为英文标点。**</mark>
{% endhint %}

1. **按章节数量筛选：**

expected\_number\_of\_chapters: 1（只筛选一发完）

&#x20;-expected\_number\_of\_chapters: 1（只筛选多章）

2. **按作者筛选：**

creators: 用户名（单独筛选某用户的作品）

-creators: 用户名（去除某用户的作品）

3. **洁癖筛选：**

otp: true（筛选出来的作品只打一对CP的标签，会筛选掉所有A/B是背景板或A/B但有其他配对的作品）

4. **不含配对筛选：**

-relationship\_ids: \*（筛选出不含任何CP或CB配对标签的作品）

<details>

<summary><strong>其他筛选法则：</strong></summary>

1. **按是否仅登录用户可见筛选：** restricted: true（是）restricted: false（不是）
2. **按作品皮肤筛选：** work\_skin\_id: 277（应用了某一个特殊作品皮肤的作品）
3. **按导入站点筛选：** imported\_from\_url: xyz（筛选出从xyz网址导入的作品，比如“username.dreamwidth.org”）
4. **按字符串筛选：** notes: 字符串**或**endnotes: 字符串（筛选出开头附注或结尾附注里含有你输入的字符串的作品，可以使用""进行精确搜索）；summary: 字符串（筛选出简介里含有你输入的字符串的作品）；series.title: 字符串（筛选出系列名称中含有你输入的字符串的作品）
5. **筛选出日期回溯的作品：**&#x62;ackdate: true（回溯了）backdate: false（没回溯）
6. **按是否在合集内筛选：**&#x63;ollection\_ids: \*（筛选出在合集内的作品）
7. **按是否是系列文筛选：**&#x73;eries.title: \*（筛选出系列文）-series.title: \*（筛选出非系列文）

</details>



### 排序依据（Sorting）

_——由你自己选择作品排序。_

虽然这一点在Filter也能做到，但是与上述两种运算符结合，能够同时进行排序与复杂筛选。

默认的排序方式是按更新日期排序，最新更新在前。

{% hint style="danger" %}
<mark style="color:red;">**注意：这里使用的标点符号均为英文标点。**</mark>
{% endhint %}

* **按字数**：

sort:words（由多到少）

sort:>words（由少到多）

* **按标题**：

sort:title（由A到Z）

sort:\<title（由Z到A）

* **按作者**：

sort:author（由A到Z）

sort:\<author（由Z到A）

* **按实际发布日期**：

sort:posted（最新发布在前）

sort:>posted（最早发布在前）

* **按更新日期**：

sort:updated（最新更新在前）

sort:>updated（最早更新在前）

* **按互动排序**：

sort:kudos（最多点赞在前）

sort:>kudos（最少点赞在前）

同理，kudos也可换成bookmarks（书签收藏）、hits（点击量）或comments（评论）

* **限定范围**：

words:1000（恰好1000字的作品）

words>1000（1000字以上的作品）；words<1000（1000字以下的作品）

words:1000-5000（1000字到5000字之间的作品）



### 总结

如果我想找到一篇配对为A/B且没有其他配对的、标签中含有「小甜饼」、字数在5000以下的作品，并按点赞数由高到低排序，那么我的搜索输入为：

<mark style="color:green;">A/B</mark> <mark style="color:orange;">AND</mark> <mark style="color:green;">fluff</mark> <mark style="color:orange;">otp: true</mark> <mark style="color:purple;">words<5000</mark> <mark style="color:yellow;">sort:kudos</mark>



资料来源：AO3的Hidden search operators cheatsheet：[https://archiveofourown.org/admin\_posts/10851](https://archiveofourown.org/admin_posts/10851)
