# 深入浅出可视化文档编辑器

## 简介
语雀提供的**可视化文档编辑器**（下文简称为「编辑器」）上线已经有一段时间，相信各位已经对它有所熟悉。
本文尝试通过一系列输入示例，将编辑器深藏的各种功能，一一展示并传授给大家。

## 键盘快捷方式
键盘快捷方式是每一款文档编辑器必不可少的基本功能，语雀的编辑器当然会内置大量快捷方式。
大部分快捷方式都遵循业界的标准，很多可能你已经早已掌握，如对字体加粗是 `Ctrl + b` 。

### 格式 
| 示例 | macOS 快捷键 | Windows 快捷键 | Linux 快捷键 |
| :--- | :--- | :--- | :--- |
| **我是粗体** | `⌘` + `b`  | `Ctrl` + `b`  | `Ctrl` + `b`  |
| _我是斜体_ | `⌘` + `i` | `Ctrl` + `i` | `Ctrl` + `i`  |
| ++我是下划线++ | `⌘` + `u` | `Ctrl` + `u` | `Ctrl` + `u`  |
| ~~我是删除线~~ | `⌘` + `Shift` + `x`  | `Ctrl` + `Shift` + `x`  | `Ctrl` + `Shift` + `x`   |
| [我是链接](https://yuque.com/yuque/help/dive-into-yuque-editor) | `⌘` + `k`  | `Ctrl` + `k`  | `Ctrl` + `k`  |

### 对齐方式

<div class="bi-table">
 <table>
   <colgroup><col width="90px"><col width="90px"><col width="90px"><col width="90px"></colgroup>
   <tbody>
    <tr>
      <td><div data-type="p">示例</div></td>
      <td><div data-type="p">macOS 快捷键</div></td>
      <td><div data-type="p">Windows 快捷键</div></td>
      <td><div data-type="p">Linux 快捷键</div></td>
    </tr>
    <tr>
      <td><div data-type="p">左对齐</div></td>
      <td><div data-type="p"><code>⌘</code> + <code>Shift</code> + <code>l</code> </div></td>
      <td><div data-type="p"><code>Ctrl</code> + <code>Shift</code> + <code>l</code> </div></td>
      <td><div data-type="p"><code>Ctrl</code> + <code>Shift</code> + <code>l</code> </div></td>
    </tr>
    <tr>
      <td><div data-type="alignment" data-value="center" style="text-align:center;"><div data-type="p">居中对齐</div></div>
</td>
      <td><div data-type="p"><code>⌘</code> + <code>Shift</code> + <code>c</code> </div></td>
      <td><div data-type="p"><code>Ctrl</code> + <code>Shift</code> + <code>c</code> </div></td>
      <td><div data-type="p"><code>Ctrl</code> + <code>Shift</code> + <code>c</code> </div></td>
    </tr>
    <tr>
      <td><div data-type="alignment" data-value="right" style="text-align:right;"><div data-type="p">右对齐</div></div>
</td>
      <td><div data-type="p"><code>⌘</code> + <code>Shift</code> + <code>r</code> </div></td>
      <td><div data-type="p"><code>Ctrl</code> + <code>Shift</code> + <code>r</code> </div></td>
      <td><div data-type="p"><code>Ctrl</code> + <code>Shift</code> + <code>r</code> </div></td>
    </tr>
    <tr>
      <td><div data-type="alignment" data-value="justify" style="text-align:justify;"><div data-type="p">两端对齐</div></div>
</td>
      <td><div data-type="p"><code>⌘</code> + <code>Shift</code> + <code>j</code> </div></td>
      <td><div data-type="p"><code>Ctrl</code> + <code>Shift</code> + <code>j</code> </div></td>
      <td><div data-type="p"><code>Ctrl</code> + <code>Shift</code> + <code>j</code> </div></td>
    </tr>
   </tbody>
 </table>
</div>

### 列表

<div class="bi-table">
 <table>
   <colgroup><col width="90px"><col width="90px"><col width="90px"><col width="90px"></colgroup>
   <tbody>
    <tr>
      <td><div data-type="p">示例</div></td>
      <td><div data-type="p">macOS 快捷键</div></td>
      <td><div data-type="p">Windows 快捷键</div></td>
      <td><div data-type="p">Linux 快捷键</div></td>
    </tr>
    <tr>
      <td><ol start="1" data-type="ordered-list">
<li data-type='list-item' data-list-type='ordered-list'><div data-type="p">有序列表</div><ol start="1" data-type="ordered-list">
<li data-type='list-item' data-list-type='ordered-list'><div data-type="p">有序列表</div></li>
<li data-type='list-item' data-list-type='ordered-list'><div data-type="p">有序列表</div><ol start="1" data-type="ordered-list">
<li data-type='list-item' data-list-type='ordered-list'><div data-type="p">有序列表</div></li>
</ol></li>
</ol></li>
<li data-type='list-item' data-list-type='ordered-list'><div data-type="p">有序列表</div></li>
</ol></td>
      <td><div data-type="p"><code>⌘</code> + <code>Shift</code> + <code>7</code> </div></td>
      <td><div data-type="p"><code>Ctrl</code> + <code>Shift</code> + <code>7</code> </div></td>
      <td><div data-type="p"><code>Ctrl</code> + <code>Shift</code> + <code>7</code> </div></td>
    </tr>
    <tr>
      <td><ul data-type="unordered-list">
<li data-type='list-item' data-list-type='unordered-list'><div data-type="p">无序列表</div><ul data-type="unordered-list">
<li data-type='list-item' data-list-type='unordered-list'><div data-type="p">无序列表</div></li>
<li data-type='list-item' data-list-type='unordered-list'><div data-type="p">无序列表</div><ul data-type="unordered-list">
<li data-type='list-item' data-list-type='unordered-list'><div data-type="p">无序列表</div></li>
</ul></li>
</ul></li>
<li data-type='list-item' data-list-type='unordered-list'><div data-type="p">无序列表</div></li>
</ul></td>
      <td><div data-type="p"><code>⌘</code> + <code>Shift</code> + <code>8</code></div></td>
      <td><div data-type="p"><code>Ctrl</code> + <code>Shift</code> + <code>8</code> </div></td>
      <td><div data-type="p"><code>Ctrl</code> + <code>Shift</code> + <code>8</code> </div></td>
    </tr>
   </tbody>
 </table>
</div>

### 插入
| 示例 | macOS 快捷键 | Windows 快捷键 | Linux 快捷键 |
| :--- | :--- | :--- | :--- |
| 提及他人 @展新展新(pizn)  | `@`  | `@`  | `@`  |

### 编辑
| 示例 | macOS 快捷键 | Windows 快捷键 | Linux 快捷键 |
| :--- | :--- | :--- | :--- |
| 保存草稿 | `⌘` + `s`  | `Ctrl` + `s`  | `Ctrl` + `s`  |
| 撤销 | `⌘` + `z`  | `Ctrl` + `z`  | `Ctrl` + `z`  |
| 重做 | `⌘` + `y`  | `Ctrl` + `y`  | `Ctrl` + `y`  |

## 插入图片
编辑器支持 N 种插入图片的方式，总有一种满足你的编写习惯。

### 顶部 toolbar 插入
![image.png | left | 113x98](https://private-alipayobjects.alipay.com/alipay-rmsdeploy-image/skylark/2018/png/e6c721bd-2e21-4083-8690-a853006e2055.png "")
这是最傻瓜的方式，点击「插入图片」，然后选择一张心仪的图片即可。

### 粘贴图片
这是最 geek 的方式，通过系统截图，或者钉钉截图，或者 QQ 截图等等截图工具，又或者在钉钉聊天窗口，右键复制一张图片，你的图片就已经保存在张贴板里面，然后你只需要右键「粘贴」，或者 `Ctrl` + `v` 快捷粘贴，图片就出来了。
![image.png | left | 429x328](https://gw.alipayobjects.com/zos/skylark/a5f63572-4d33-44e8-a5aa-868e34f4118c/2018/png/e597aa4c-2711-46b0-9dcc-b6f2d00b13c4.png "")

### 粘贴图片 URL
如果你已经复制好了一个图片 URL，如 `https://gw.alipayobjects.com/foo.jpg` ，你只需要右键「粘贴」，或者 `Ctrl` + `v` 快捷粘贴，图片就出来了。

![image | left](https://gw.alipayobjects.com/zos/skylark/8ceb0099-8b84-4d23-877d-19222c5893d1/2018/jpg/fd96a593-402f-4c56-ade2-c4f856975391.jpg "")

### 拖拽图片文件
这是最直接的操作方式，从文件夹将图片文件直接拖拽进编辑器，图片就出来了。

![image.png | left | 306x170](https://gw.alipayobjects.com/zos/skylark/d4945fab-08d3-4087-8758-a80d0b8343a0/2018/png/8773815d-491b-4a00-b1e0-ed274046776e.png "")

### 图片缩放
点击选中图片，会出现图片相关操作提示，通过右下角可以拖动图片。
![image.png | left | 496x311](https://lark-assets-prod.oss-cn-hangzhou.aliyuncs.com/2018/png/1c08740e-e33e-4649-ae49-308e8687eb1b.png "")
![image | left | 375x250](https://static.dingtalk.com/media/lAHPBbCc1VHhgvXNATfNAdU_469_311.gif "")

## 插入链接

插入链接也有非常多种形式，可以从工具栏上选择『插入链接』，也可以选中文字后从弹出的工具条上点击『插入链接』将这段选中文字变成链接。下面推荐两个更快速的给文字加超链接的方式。

### 快捷键添加链接

1. 选中文字
2. 通过快捷键 `⌘ + k` 直接将文字变成链接（Windows 下快捷键为 `Ctrl + k`）
3. 编辑超链接地址


### 复制粘贴链接

1. 复制链接地址
2. 选中文字
3. 粘贴链接，直接将选中文字附上链接

![image | left](https://gw.alipayobjects.com/zos/skylark/99a72a37-d0de-4c2c-894c-aa5b2c5caef9/2018/gif/ebdb6279-7dab-40ad-a1ce-520ae0d3c82a.gif "")

## 插入表情（Emoji） 🎉

直接输入冒号 `:` ，会弹出表情选择器，可以愉悦地选择你需要的表情。目前提供的表情比较少，后续会不断丰富完善。

![image | left](https://gw.alipayobjects.com/zos/skylark/d1434706-02ee-4181-aeb0-b3b08cbc2002/2018/png/d8d27794-74b1-4780-b6b7-5846634377a3.png "")

## Markdown 输入法
语雀支持绝大部分的 markdown 快捷输入方式，通过这些快捷输入方式，我们可以不用鼠标完成文档的编辑。  

![Kapture 2018-01-18 at 11.41.07.gif | center | 752x493](https://lark-assets-prod.oss-cn-hangzhou.aliyuncs.com/2018/gif/8255c56e-8525-49b2-9690-d1c8318d5e45.gif "")
### 快捷输入对照表
| 示例 | 快捷输入 |
| :--- | :--- |
| # 大标题，技术范叫 H1
 | `#` + `Space` + `文本` ，魔法就会发生 |
| ## 中标题，对，H2
 | `##` + `Space` + `文本`  |
| ### 小标题，H3
 | `###` + `Space` + `文本`  |
| 1. 有序列表

 | `1` + `.` + `Space` + `文本` ，魔法又发生，尝试回车和 `tab` 看看更多神奇的效果吧。 |
| * 无序列表

 | `-` + `Space` + `文本` ，当然也可以使用 `\*` 代替 `-`  |
| * [ ] 未完成任务列表

 | `[` + `]` + `Space` + `文本` ，秒建 TODO 功能 |
| * [x] 已完成任务列表

 | `[` + `x` + `]` + `文本` ，任务完成！😊 |
| > 引用文本，引用名人名句，引用大大的发言

 | `>` + `Space` + `文本`  |
| 快速创建表格 | `|` + `A` + `|` + `B` + `|` + `回车` ，快速创建两列表格 |
| 快速创建代码块 | 连续 3 个 ````` + `回车` ，出现工程师最😍的代码块  |
| 长长的分割线 | 连续 3 个 `-` + `回车` ，会出现一条长长的分割线 |
| **粗体文本**  | `\*` + `\*` + `文本` + `\*` + `\*` + `Space` ，文本变粗！ |
| _斜体文本_  | `\_` +_ _`文本` + `\_` + `Space` ，文本变右倾斜了。 |
| ~~删除线~~  | `~` + `~` + `文本` + `~` + `~` ，显示地给文字加删除线 |
| `行内代码 foo = bar`  | ````` + `代码文本` + ````` + `Space`，不明白程序员为何就喜欢写代码 |
| 上标 21^th^ 1^st^ 邮票 ^🎫^  | `^` + `文本` + `^` + `Space` ，文本飘上去了 |
| 下标 H~2~O 是水，化学没白学 | `~` + `文本` + `~` + `Space` ，各种公式少不了的技能 |
| ==高亮，亮瞎眼的文本==  | `=` + `=` + `文本` + `=` + `=` ，就像荧光笔一笔划过 |

### 复制 Markdown 格式文本
* 在阅读页面，右上角「更多」里面可以找到「查看源码」。
  ![image | center](https://gw.alipayobjects.com/zos/skylark/cfaa3ff5-f469-4096-91ec-8a8b5dce7e92/2018/png/f1f3158b-5f24-4d06-98e4-12d268015081.png "")

![image | center](https://gw.alipayobjects.com/zos/skylark/4722b154-c062-4219-9537-a705b0b3e8af/2018/png/c59a2503-3757-4d4c-b779-fd0d77a392e8.png "")

## PlantUML 图

请到「[PlantUML 图](https://yuque.com/yuque/help/puml)」章节查看。

## 数学公式

请到 「[数学公式](https://yuque.com/yuque/help/katex)」章节查看。

## 导入 Word、Markdown 文档
在文档菜单中，选择从 Word、Markdown 文档新建，可以让你快速选择本地已有的 Word 、Markdown 文档导入到语雀中。

![image | center](https://gw.alipayobjects.com/zos/skylark/4e0421bd-5161-4dd7-8c16-f17781ca480b/2018/gif/5386abad-ce46-4f7f-9056-e2fc50ed03a6.gif "")

<span style="color:#F5222D;">_**注意**_</span>_**：Word 导入目前只支持语雀可以识别的文档格式。**_

## 更多特性
未完，待续...

