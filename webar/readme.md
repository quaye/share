# 了解历史：web前端30年

## 1. 序章

> 声明：本文不保证所述内容精准无误，若发现问题，请及时issue。  
> 小问题：英特网、万维网？

## 2. 概念

### 2.1 web前端是什么

很沮丧，在 [wiki][link-wiki] 上并没有找到关于 **front-end web（web前端）** 的准确定义，我们可以从 **[Front and back ends(前后端)][link-Front_and_back_ends]** 入手，结合 **[Front-end web development（前端开发）][link-Front-end_web_development]** 、**[Web application(web app)][link-Web_application]** 的定义，“综合归纳”后给出自己理解的定义。

#### 2.1.1 [Front and back ends(前后端)][link-Front_and_back_ends]

In software engineering, the terms **front end** and **back end** refer to the separation of concerns between the presentation layer (front end), and the data access layer (back end) of a piece of software, or the physical infrastructure or hardware. In the client–server model, the client is usually considered the front end and the server is usually considered the back end, even when some presentation work is actually done on the server itself.

- 在软件、硬件、基础设施上，表现层称之为“前端”，数据存取（处理）层称之为“后端”。  
- 在客户机-服务器模型(后文简称C/S)上：客户机通常被认为是“前端”，服务器通常被认为是“后端”。

#### 2.1.2 [Front-end web development(web前端开发)][link-Front-end_web_development]

Front-end web development is the **practice** of converting data to a graphical interface, through the use of HTML, CSS, and JavaScript, so that users can view and interact with that data.

- 定义：是一种用特定技术（html/js/css），把数据转换为图形接口**行为**。
- 目的：为了便于用户查看数据、与数据交互。

#### 2.1.3 [Web application(web app / web应用)][link-Web_application]

In computing, a web application or web app is a client–server computer program that the client (including the user interface and client-side logic) runs in a web browser. Common web applications include webmail, online retail sales, online banking, and online auction

- 定义：指明C在浏览器中运行的C/S架构的计算机程序并指明
- 附加：根据<2.1.1>可知这里的C属于“前端”

#### 2.1.4 重新认识并定义 Front-end web (web前端)

- 重新定义：web前端是运行在浏览器下的 C/S 计算机程序中的C(包括用户界面和客户端逻辑）。是利用特定技术（js/**html**/css...）将数据转化成的“用户图形接口（GUI）”。

### 2.2 万维网的三大核心技术

在wikipad的 [World Wide Web(WWW)][link-WWW]描述中，有这样一句话：Hypertext Markup Language (HTML) is the standard markup language for creating web pages and web applications. With Cascading Style Sheets (CSS) and JavaScript, it forms a triad of cornerstone technologies for the World Wide Web（概要：HTML、CSS、JavaScript是组成万维网的三大核心技术）。

> 补充1：[WWW][link-WWW]标准目前由[W3C][link-W3C]维护。  
> 补充2：[WWW（World Wide Web）][link-WWW]是我们俗称的web网络服务（万维网）。  
> 补充3：[W3C（World Wide Web Consortium）][link-W3C]是负责万维网标准的维护的组织。

#### 2.2.1 [Hypertext Markup Language (HTML)][link-html]

[Hypertext Markup Language (HTML)][link-html] is the standard markup language for documents designed to be displayed in a web browser.

- 定义：**HTML是一种**用于在web浏览器中显示的文档的标准**标记语言**。
- 作用：控制文档结构。

> **特别说明：[HTML][link-html] 绝不是 [HTML5][link-html5] ！！！**
>
> HTML5 is a software solution stack that defines the properties and behaviors of web page content by implementing a markup based pattern to it.
>
> - 定义：**HTML5是** 定义了通过标记模式实现web页面的属性、行为内容的 **软件解决方案集**。
>
> 补充1：由万维网联盟（W3C）于2014年10月完成标准制定。  
> 补充2：HTML5是一个标准，该标准由各浏览器厂商自行实现。  
> 补充3：HTML5是一个标准集，提供了多种组件，方便了web页面的开发。  
> 补充4：HTML是标记语言，仅属于web前端开发中所使用到工具的一种，二者绝无可能划等号。

#### 2.2.2 [Cascading Style Sheets (CSS)][link-CSS]

[Cascading Style Sheets (CSS)][link-CSS] is a style sheet language used for describing the presentation of a document written in a markup language like HTML.

- 定义：**CSS是一种**用于描述标记语言(例如：html)所述文档的表示形式的 **样式表语言**。
- 作用：修饰标记语言（HTML）所展示的元素。

#### 2.2.3 [JavaScript][link-js]

[JavaScript][link-js] often abbreviated as JS, is a high-level, just-in-time compiled, object-oriented programming language that conforms to the specification.  

[ECMAScript (or ES)][link-ECMAScript] is a scripting-language specification standardized by Ecma International in ECMA-262 and ISO/IEC 16262. It was created to standardize JavaScript to help foster multiple independent implementations.

- 定义：**js是**基于ECMAScript标准实现的高级的、即时编译、弱类型、基于原型的面向对象的 **脚本语言**。
- 作用：常用来给HTML网页添加动态功能（例如用户操作、数据处理），也可以用于其他场合，如服务器端编程。

> 补充1：javascript和java有关系吗？答：没半毛钱关系。Javascript 是 [Netscape][link-Netscape] 公司的脚本语言；Java 是 [SUN Microsystems][link-sun] 公司推出的面向对象的程序设计语言。  
> 补充2：网传害人！看看正史小故事。1995年，Netscape招募了布兰登·艾克（Brendan Eich），目标是把Scheme语言嵌入到Netscape Navigator浏览器当中。但更早之前，Netscape已经跟 SUN 合作在Netscape Navigator中支持Java。后来Netscape决定发明一种与Java搭配使用的辅助脚本语言并且语法上有些类似。为了在其他竞争提案中捍卫JavaScript这个想法，公司需要有一个可以运作的原型。艾克（Brendan Eic）在1995年5月仅花了十天时间就把原型设计出来了。最初命名为 ‘Mocha’，1995年9月在Netscape Navigator 2.0的Beta版中改名为 ‘LiveScript’，同年12月，Netscape Navigator 2.0 Beta 3中部署时被重命名为‘JavaScript’，当时Netscape公司与sun公司组成的开发联盟为了让这门语言搭上Java这个编程语言“热词”，因此将其临时改名为JavaScript，日后这成为大众对这门语言有诸多误解的原因之一。

## 3 浏览器

网页浏览器（英语：[Web Browser][link-Web_browser]，常简称为浏览器）是一种用于检索并展示万维网信息资源的应用程序(是所见即所得网页编辑器)。这些信息资源可为网页、图片、影音或其他内容，它们由统一资源标志符标识。信息资源中的超链接可使用户方便地浏览相关信息。

### 3.1 浏览器历史（仅名气大的）

- 1990年 《[WorldWideWeb (Nexus)][link-Nexus]》蒂姆·伯纳斯-李(Timothy John Berners-Lee)。
  
> oh my god 001: 世界上第一个网页浏览器,后来为了避免与万维网混淆而改名为Nexus

- 1993年 《[Mosaic][link-Mosaic]》 马克·洛厄尔·安德森（Marc Lowell Andreessen）
- 1994年 《[Netscape Navigator][link-Netscape_Navigator]》Netscape
- 1995年 《[Internet Explorer ( 简称 IE )][link-Internet_Explorer]》Microsoft
  
> oh my god 002: [第一次浏览器大战（1995–2001）][link-Browser_wars] 《IE》 (胜) vs（败）《Netscape Navigator》

- 1996年 《[Opera][link-Opera]》挪威电信（Telenor ASA)
- 2002年 《[Mozilla Application Suite 1.0（Mozilla）][link-Mozilla_Application_Suite]》 Netscape 开源作品
- 2002年 《[Mozilla Phoenix][link-Firefox#History]》 Mozilla 社群的一个分支 (Firefox的前身)
- 2003年 《[Safari][link-Safari]》 Apple Inc. 基于KDE的[KHTML排版引擎][link-KHTML]

> oh my god 003: 2003年7月15日 Netscape 公司gg  -_-!! 请牢记 Netscape 的 Mozilla。

- 2004年 《[Mozilla Firefox (通称 Firefox)][link-Firefox]》 Mozilla基金会 代表Netscape灰烬中浴火重生
- 2008年 《[Google Chrome][link-Google_Chrome]》 Google LLC，基于[WebKit排版引擎][link-WebKit](2014年切换至[blink渲染器][link-blink])和[Mozilla Firefox][link-Firefox],自研[V8][link-V8]
- 2015年 《[Microsoft Edge][link-Microsoft_Edge]》 Microsoft ;2018年后基于Chromium开发

> oh my god 004: [第二次浏览器大战（2004–2017）][link-Browser_wars] 《Chrome》 （胜） vs （中）《Firefox》 vs （中）《IE》 vs （中）《Safari》 vs （无视？）《Opera》

### 3.2 影响巨大的浏览器

- **[IE][link-Internet_Explorer]** : IE是微软公司旗下浏览器，是目国内用户量最多的浏览器。IE诞生于90年代，当时微软为了对抗市场份额占据将近百分之九十的网景Netscape Navigator，于是在Windows中开发了自己的浏览器Internet Explorer，自此也引发了第一次浏览器大战。微软以IE和Windows捆绑的模式不断向市场扩展份额，使IE成为市场的绝对主流。现在装了Windows系统的电脑基本无法卸载IE。

- **[Opera][link-Opera]** ：Opera是挪威Opera Software ASA公司旗下的浏览器。1996年，opera公司发布第一版Opera浏览器，使用自己研发的Presto内核。当时opera公司的开发团队不断完善Presto内核，使Opera浏览器一度成为顶级浏览器。直到2016年奇虎360和昆仑万维收购了Opera浏览器，从此也丢弃了强大的Presto内核，改用当时Google开源的webkit内核。后来Opera浏览器跟随Google将浏览器内核改为Blink内核。自此Presto内核也淡出了互联网市场。

- **[Safari][link-Safari]** :第二次浏览器大战是从苹果公司发布Safari浏览器开始的。2003年，苹果公司在苹果手机上开发Safari浏览器，利用自己得天独厚的手机市场份额使Safari浏览器迅速成为世界主流浏览器。Safari是最早使用webkit内核的浏览器也是现在苹果默认的浏览器。

- **[Firefox][link-Firefox]** : Firefox浏览器是Mozilla社区产物。Firefox采用Gecko作为内核。Gecko是一个开源的项目，代码完全公开，因此受到很多人的青睐。Firefox的问世加快了第二次浏览器大战的开始。第二次浏览器大战与第一次二元鼎力的局面不同，这一次的特点就是百家争鸣，也自此打破了IE浏览器从98年网景被收购后独步浏览器市场的局面。

- **[Chrome][link-Google_Chrome]** ：Chrome浏览器是google旗下的浏览器。Chrome浏览器至发布以来一直讲究简洁、快速、安全，所以Chrome浏览器到现在一直受人追捧。最开始Chrome采用webkit作为浏览器内核，直到2013年，google宣布不再使用苹果的webkit内核，开始使用webkit的分支内核Blink。

- **[Edge][link-Microsoft_Edge]** ： 2015年4月30日，微软在旧金山举行的Build 2015开发者大会上宣布，其最新操作系统——Windows 10内置代号为“Project Spartan”的新浏览器被正式命名为“Microsoft Edge”，其内置于Windows 10版本中。2018年3月，微软宣布登陆iPad和安卓平板。这意味着Edge浏览器已经覆盖了桌面平台和移动平台。采用的内核为EdgeHTML。

### 3.3 浏览器市场占比

- [全球-浏览器使用率统计][link-statcounter_all]  

    ```text
    * 注意：本区域为占位块，方便查阅，真实数据请[点击]"全球-浏览器使用率统计"
    |  _____
    | /     \      /
    |/       \____/
    |_______________

    ```

- [国内-浏览器使用率统计][link-statcounter_chaina]

    ```text
    * 注意：本区域为占位块，方便查阅，真实数据请[点击]"国内-浏览器使用率统计"
    |  _____
    | /     \      /
    |/       \____/
    |_______________

    ```

> 补充：浏览器的其他对比请参见 [WiKi][link-Comparison_of_web_browsers] ，本文仅列出浏览器市场占有率。

### 3.4 浏览器组成

![浏览器结构](/webar/doc/browser-layer.png)

<!-- markdownlint-disable MD033 -->

模块功能简述:

- User Interface    : 主要提供用户与Browser Engine交互的方法。

- Browser Engine    : 协调 UI 和 the Rendering Engine，在他们之间传输指令。

- Rendering Engine  : 解析JavaScript、Html、Xml，并且User Interface中展示的layout。

- Networking        : 基于互联网HTTP和FTP协议，处理网络请求。

- JavaScript Interpreter :解释和运行网站上的js代码，得到的结果传输到Rendering Engine来展示。

- UI Backend        : 用于绘制基本的窗口小部件,底层使用操作系统的用户界面方法，平台无关的接口。

- Data Storage      : 管理用户数据，例如书签、cookie和偏好设置等。

chrome浏览器运行时进程模型说明：

![browser-archive](/webar/doc/browser-archive.png)

#### 3.4.1 著名浏览器架构

- Chrome 架构
![Arch_Chrome](/webar/doc/Arch_Chrome.png)

- FireFox 架构
![Arch_FireFox](/webar/doc/Arch_FireFox.png)

#### 3.4.2 弃用名次“内核”，使用专业名次“渲染引擎（或呈现引擎）+ js解释器”

> - 补充1：在浏览器环境中，我们通常将渲染引擎称呼为：Browser engine（浏览器引擎）、layout engine（排版引擎）、rendering engine（渲染引擎、呈现引擎）；它们都是一个东西。  
> - 补充2：早些年代，渲染引擎（呈现器）设计中，包含了js解析器的功能，js解析器也被设计为专为浏览器服务，但随着后来V8的独立和流行，称呼chrome内核 = webkit（仙子啊时blink）+v8引擎，但是早年的排版引擎未被淘汰，导致了如今称呼的（内核）理解混乱的根本。  
> - 补充3：国内常用的一种称呼“浏览器内核”,特指 “rendering engine 和 js Interpreter”,但这样的称呼 **很不专业**，因为wiki上压根没有“浏览器内核”这个词的解释。  
> - 补充4：对于 Rendering engine 和 Browser engine 在真实的浏览器架构中，完全指的是两部分，对“补充1（来自wiki）”并不矛盾，但在表述“渲染引擎（或呈现引擎）”时，尽量使用“渲染引擎（或呈现引擎）” ，避免使用有歧义的“Browser engine”。

##### 3.4.3 知名的渲染引擎（呈现引擎）

对于渲染引擎来说，其核心作用：**负责获取标记式内容（如HTML、XML及图像文件等等）、整理信息（如CSS及XSL等），并将排版后的内容输出至显示器或打印机**，目前知名的渲染引擎列出如下。

- Trident，又叫 MSHTML
  - 出处：是Microsoft开发的一种排版引擎。
  - 代表：IE、傲游、世界之窗浏览器、Avant、腾讯TT、猎豹安全浏览器、360极速浏览器...

- Gecko
  - 出处：Gecko开源，原本由Netscape开发，现在则由Mozilla基金会维护。
  - 代表：Mozilla FireFox(火狐浏览器) 采用该排版引擎。

- webkit：
  - 出处：基于 [KHTML][link-KHTML] 的分支，Apple开发的排版引擎，
  - 代表：Apple Safari (Win/Mac/iPhone/iPad)、Android 默认浏览器，傲游浏览器3...

- Blink：
  - 出处：基于 webkit 的分支在
  - 代表：chrome、others ............

- Presto：
  - 出处：Opera Software开发的网页浏览器排版引擎
  - 代表：opera的"前任"...

> 补充1：国内大部分浏览器基于[chromium][link-chromium]（采用Blink）开发。  
> 补充2：国内浏览器所谓双核心（"兼容模式"），指的是同时采用了两个渲染引擎。

#### 3.4.4 渲染引擎（呈现引擎）工作原理

设想一下，当我们自己制作一个《浏览器》的渲染模块时应该设计怎样的流程，或许能更好的理解。

浏览器从网络层获取请求的文档内容，然后开始渲染流程如下：

![Arch_Chrome](/webar/doc/browser-workflow.png)

- 解析并开始构建 content tree（element --> DOM nodes），同时解析样式数据（外部CSS和style元素）；
- 两者结合构建 render tree（渲染树包含带有视觉属性（如颜色和尺寸）的矩形们）
- 在渲染树创建后进入 Layout 阶段，给渲染树的每个节点设置在屏幕上的位置信息
- Paint 阶段，通过 UI backend 绘制 render tree 到屏幕。

具体渲染流程，参见细节[《Inside look at modern web browser》][ref-01]，过程如下：

![web-file-load-flow](/webar/doc/web-file-load-flow.jpg)

当然对于不同的浏览器来说，其渲染流程也略有不同，

- webkit 构建过程  
![renderflow-webkit](/webar/doc/renderflow-webkit.png)

- gecko 构建过程  
![renderflow-gecko](/webar/doc/renderflow-gecko.png)

### 3.5 JavaScript引擎

JavaScript引擎是一种计算机程序，其执行的JavaScript（JS）的代码。第一个JavaScript引擎仅仅是解释器，但是所有相关的现代引擎都利用即时编译（just-in-time，JIT）来提高性能。JavaScript引擎通常是由Web浏览器供应商开发的，每个主要的浏览器都有一个。在浏览器中，JavaScript 引擎通过Document Object Model与渲染引擎协同运行。但JavaScript引擎不仅限于浏览器还有可以在服务端运行的运行时系统 Node.js（V8引擎是Node的核心组件）。

#### 3.5.1 知名的JavaScript引擎

- [SpiderMonkey][link-SpiderMonkey] （C++开发）:
  - 出处：（1995）Mocha：[Netscape][link-Netscape]的艾克（Brendan Eic）10撸成。
  - 出处：（1996）SpiderMonkey：艾克（Brendan Eic）重撸，现由Mozilla社区维护
  - 代表：Firefox、GNOME、Adobe系列...

- [Rhino][link-Rhino] （Java开发）:
  - 出处：（1997）Mocha：[Netscape][link-Netscape]遗产，现由Mozilla社区维护。
  - 代表：未完成的Netscape Navigator（java版）gg了。

- [V8][link-V8] （C++开发）
  - 出处：（2008）google 的 Lars Bak 创建的[开源js引擎][link-V8-org]
  - 代表：chrome、MongoDB、Node.js、others ................................

- [JavaScriptCore][link-JavaScriptCore]
  - 出处：基于KJS开发，Apple 维护。
  - 代表：WebKit。

- [Chakra][link-Chakra]
  - 出处：Microsoft
  - 代表：IE、Microsoft Edge

> 补充1：作为一个语言引擎，要具备 加载文件、编译能力、解释能力甚至优化能力，具体请参见[《how-javascript-works-inside-the-v8》][how-javascript-works-inside-the-v8]  
> 补充2：[MDN][link-mdn]是Mozilla开发者网站，是学习HTML/CSS/javascript的好去处，山寨害死人，多看官方文档。  
> 补充3：BOM（Browser Object Model）使用 js 来操作浏览器对象的API。
> 补充4：DOM（Document Object Model）使用 js 来操作HTML/XML对象的API。
> 补充5：如果 3、4 没有理解，那就把BOM/DOM理解为 dll / lib 一组还有n个API的库。

## 4 Web前端开发

### 4.1 需求改变前端技术

> ---------------- WEB 0.0 时代 in ---------------- 从无到有（不知道）

需求:在欧洲粒子物理实验室（粒子物理研究通常与来自世界各地的研究所进行合作）IT部门工作的Tim Berners-Lee提出：使来自世界各地的远程站点的研究人员能够组织和汇集信息，在个人计算机上访问大量的科研文献，并建议在文档中链接其他文档

- 1990  - 《[WorldWideWeb (Nexus)][link-Nexus]》  ~  1993 《[Mosaic][link-Mosaic]》
  - 【 HTML1.0 】IETE(internet engineering tesk force,因特网工程任务组)，其实这个规范并不存在

- 1991
  - 【 HTTP 0.9 】

- 1994 - 《W3C》

  - 【 HTTP 1.0 】

> ---------------- 0 时代 in ---------------- 仅能阅读（陌生人）

需求: 纯静态页面，网页仍然只读，只能从服务器到客户端单向流通？（所有人请求结果都一样）  
需求：撸代码，咱俩写的咋不大一样？

- 1995
  - 【 HTML2.0 】IETE官方规范
  - 【 javascript 】Brendan Eich，让js来修改dom样式（交互问题得到解决）
  - 【 PHP （Hypertext Preprocessor）】动态服务器页面技术，“php是世界上最好的语言！”web鄙视链的伊始

- 1996
  - 【 HTML3.2 】【CSS1】
  - 【 ASP（Active Server Pages） 】【 JSP（JavaServer Pages） 】动态服务器页面技术（读取sever数据）

- 1997
  - 【 HTTP 1.1 】
  - 【 ECMA-262(1) 】规范的伊始，其规范代表实现：AS/JS/JScript

- 1998
  - 【 ECMAScript2 】

- 1999
  - 【 HTML4.1 】【CSS3】
  - 【 ECMAScript3 】
  - 【 JSON 】Douglas Crockford ，在此之前，都是【XML】

- 2000
  - 【 xhtml1.0 】

- 2001
  - 【 xhtml1.1 】

- 2002
  - 【 JSLint 】解决

- 2003
  - 【 webkit 】

> ---------------- WEB 2.0 时代 in ---------------- 双向互动、虚拟身份（客人）

需求：后端重、前端轻怎么办？  
需求：每次获取数据都得刷页面？
需求：这么多的浏览器，兼容性怎么办？  
需求：JS运行效率太低了？  
需求：基本无法复用代码？  
需求：撸代码，变量冲突，顺序加载，无法解决相互依赖？  
需求：ES??各种标准如何兼容？浏览器支持的只有ES5！

- 2004
  - 【 AJAX (Asynchronous JavaScript and XML) 】（AJAX动态获取数据，不用刷新了，刚需！）
  
- 2005
  - 【 xhtml2.0 】

- 2006
  - 【 JQuery 】（解决浏览器兼容性问题,其他：Dojo、YUI、ExtJS、MooTools）
  - 【 XMLHttpRequest 标准发布（W3C）】AJAX轰炸基础奠定
  - 【 Canvas 】

- 2007
  - 【 web app 】Steve Jobs，Apple. PWA（渐进式网页应用） 的原型 : 渐进式、可响应、可离线、实现类似App的交互、即时更新、安全、可以被搜索引擎检索、可推送、可安装、可链接。

- 2008
  - 【 HTML5 】包含【 Web Worker（利用多核CPU）】【 video 】等现代技术封装组件
  - 【 V8 】【 WebSocket 】解决js运行效率问题

- 2009
  - 【 CommonJS 规范 】在浏览器环境之外构建 JavaScript 生态系统的一套规范
  - 【 AMD 标准 】浏览器环境设计的 JavaScript 模块依赖异步加载标准
  - 【 Nodejs 】磊了磊了，基于事件循环的异步I/O框架，写后台用的，前后端统一语言js
  - 【 ECMAScript5 （ES5） 】
  - 【 WebGL 1.0 】渲染3d问题

- 2010
  - 【 CSS2.1 】
  - 【 npm 】Node.js的包管理系统
  - 【 BackboneJS (MVC) 】
  - 【 Knockout (MVVM) 】
  - 【 Angularjs (MCC->MVVM) 】(google, **SPA:Single Page Application**，向着WebApp演进节点)

- 2011 - win8 系统层支持 js
  - 【 HTTP 2.0 】
  - 【 Ember.js (MVVM) 】
  - 【 Meteor (MVC) 】
  - 【 Bootstrap 】 twitter 提供创建现代响应式页面所需要的工具
  - 【 Bower 】 twitter 包管理工具
  - 【 browserify 】js的构建工具

- 2012
  - 【 TypeScript 】microsoft
  - 【 webpack 】模块化打包工具
  - 【 Grunt 】任务自动管理工具
  - 【 GraphQL 】 API 的查询语言
  - 【 webview + native 】混合应用开发大火（webview）

- 2013
  - 【 Firefox OS 】Mozilla基金会
  - 【 React （MVVM） 】
  - 【 WebGL 2.0 】
  - 【 ESLint 】摒弃【 JSLint 】

- 2014
  - 【 Vue （MVVM） 】
  - 【 gulp.js 】自动化构建工具
  - 【 Babel 】 新语法特性转码器
  - 【 Web Components 】自定义web组件API
  - 【 Service Worker 】W3C，用来做持久的离线缓存

- 2015
  - 【 React Native 】
  - 【 ECMAScript6（ES6\ES2015）】
  - 【 Service Worker 】W3C，用来做持久的离线缓存，奠定了PWA (Progressive Web App)技术基石

  > PWA 基础奠定：goole vs apple ，利益相关apple无法支持PWA。

- 2016
  - 【 Html5.1 】

- 2017
  - 【 wx-小程序 】
  - 【 workbox 】google

  > 微信跨平台，app内构建PWA，国内开始重视PWA。

- 2018
  - 【 WebAssembly 】革命性的一步参考应用《AutoCad Web》
  - 【 Web App Manifest】 Apple PWA 标准的产物

- 2019
  - 【 flutter 】 google  
  
> 2020之后将迎来------ WEB 3.0 时代 in ----------------  真实身份、从事生产（主人）

- 未来发展趋势 ：chromeos，可能是一个形态？其余尽情yy。

>补充：Web 页面与移动 App 的需求相差甚远， Web 技术仍然是当前移动 App 的架构中必备的组成部分优势在于：可链接、可访问、零门槛、独立部署、健壮性，SPA过时了，参看[《motherfuckingwebsite.com》](https://motherfuckingwebsite.com)，因此 PWA 可能是未来。

### 4.2 小程序架构原理，参考[PWA][link-pwa]技术集和标准

![wechatapp](/webar/doc/wcharapp.png)

- 小程序本身是 PWA 技术集和标准（目前还在进化中...）的大部分实现，只是PWA属于浏览器和大厂之间的斗争，小程序是国内流量入口间的斗争。

  - 渐进增强：支持的新特性的浏览器获得更好的体验，不支持的保持原来的体验
  - 离线访问：通过Service Workers可以再离线或者网速差的环境下工作
  - 类原生应用：使用app shell model做到原生应用般的体验
  - 可安装：允许用户保留对他们有用的应用在主屏幕上，不需要通过应用商店
  - 容易分享：通过URL可以轻松分享应用
  - 持续更新：受益于service worker的更新进行，应用能够始终保持更新
  - 安全：可通过https来提供服务来防止网络窥探，保证内容不被篡改
  - 可搜索：得益于W3C manifests元数据和service worker的等级，让搜索引擎能够找到wen应用
  - 再次访问：通过消息推送等特性让用户再次访问变得容易

### 4.3 [TypeScript][link-ts]与JavaScrip

TypeScript是一种由 microsoft 开发的自由和开源的编程语言。它是JavaScript的一个严格超集，并添加了可选的静态类型和使用看起来像基于类的面向对象编程语法操作 Prototype。TypeScript设计目标是开发大型应用，然后转译成JavaScript。由于TypeScript是JavaScript的严格超集，任何现有的JavaScript程序都是合法的TypeScript程序。

- javascript优点：

  - 人气：JavaScript 社区中可以很方便地找到大量成熟的开发项目和可用资源。

  - 学习曲线：由于 JavaScript 语言发展的较早，也较为成熟。

  - 本地浏览器支持：TypeScript 代码需要被编译JavaScript。

  - 灵活性：JavaScript 弱类型，想咋写咋写。

- typescript优点：

  - 强类型：手误概率低能帮助开发人员检测出错误并修改。

  - 重构方便：TypeScript工具使重构更变的容易、快捷。

  - “类”概念：TypeScript 引入了 JavaScript 中没有的“类”概念。

  - 未来编译：存在编译就有可优化空间，这将是ts未来发展趋势。

## 5 选择选择困难症：前端开发技术栈（筛选后）

本来内容来自 [WebFrontEndStack](https://github.com/unruledboy/WebFrontEndStack/blob/master/README.zh-cn.md)，经筛选，我司可能用罗列如下。

- 协议
  - [HTTP/1.1](https://www.ietf.org/rfc/rfc2616.txt)
  - [HTTP/2](https://en.wikipedia.org/wiki/HTTP/2)

- Web三剑客
  - HTML (HyperText Markup Language)
  - CSS (Cascading Style Sheets)
  - JavaScript

- 渲染引擎
  - [Trident (IE)](https://en.wikipedia.org/wiki/Trident_(layout_engine))
  - [Blink / prev. WebKit (Chrome)](http://www.chromium.org/blink)
  - [Gecko (Firefox)](https://developer.mozilla.org/en-us/docs/Mozilla/Gecko)
  - [WebKit (Safari)](http://www.webkit.org/)
  - [Blink / prev. Presto (Opera)](http://www.chromium.org/blink)
  - [EdgeHTML (Edge)](https://en.wikipedia.org/wiki/EdgeHTML)

- javascript引擎
  - [JScript (IE8- / ASP)](https://en.wikipedia.org/wiki/JScript)
  - [Chakra (IE9+ / Edge)](https://en.wikipedia.org/wiki/Chakra_(JScript_engine))
  - [V8 (Chrome / Opera / Nodejs / MongoDB)](https://developers.google.com/v8/?hl=zh-CN) [[GitHub]](https://github.com/v8/v8/)
  - [SpiderMonkey (Firefox)]( https://developer.mozilla.org/en-us/docs/Mozilla/Projects/SpiderMonkey)
  - [JavaScriptCore (Safari)](https://en.wikipedia.org/wiki/WebKit#JavaScriptCore)

- 编辑器
  - [Sublime Text](http://www.sublimetext.com/)
  - [WebStorm](https://www.jetbrains.com/webstorm/)
  - [Atom](https://atom.io/) [[GitHub]](https://github.com/atom/atom/)
  - [Vim](http://www.vim.org/)
  - [Emacs](https://www.gnu.org/software/emacs/)
  - [Brackets](http://brackets.io/) [[GitHub]](https://github.com/adobe/brackets/)
  - [Light Table](http://lighttable.com/) [[GitHub]](https://github.com/LightTable/LightTable/)
  - [Visual Studio](https://www.visualstudio.com/)
  - [Visual Studio Code](https://code.visualstudio.com/) [[GitHub]](https://github.com/Microsoft/vscode)

- 构建工具
  - [Grunt](http://www.gruntjs.com/) [[GitHub]](https://github.com/cowboy/jquery-tiny-pubsub/)
  - [Gulp](http://gulpjs.com/) [[GitHub]](https://github.com/gulpjs/gulp/)
  - [Brunch](http://brunch.io/) [[GitHub]](https://github.com/brunch/brunch/)
  - [Yeoman](http://yeoman.io/)

- 基础工具
  - [Node.js](https://nodejs.org/) [[GitHub]](https://github.com/joyent/node/)
  - [Phantom.js](http://phantomjs.org/) [[GitHub]](https://github.com/ariya/phantomjs/)
  - [SpiderMonkey](https://developer.mozilla.org/en-US/docs/Mozilla/Projects/SpiderMonkey)

- 质量控制
  - [JSLint](http://www.jslint.com/) [[GitHub]](https://github.com/douglascrockford/JSLint/)
  - [JSHint](http://jshint.com/) [[GitHub]](https://github.com/jshint/jshint/)
  - [jscs](http://jscs.info/) [[GitHub]](https://github.com/jscs-dev/node-jscs)
  - [Closure Linter](https://developers.google.com/closure/utilities/)

- 包管理
  - [npm](https://www.npmjs.com/) [[GitHub]](https://github.com/npm/npm/)
  - [Bower](http://bower.io/) [[GitHub]](https://github.com/bower/bower/)

- 库 / 框架
  - 基础库
    - [jQuery](https://jquery.com/) [[GitHub]](https://github.com/jquery/jquery/)
    - [Prototype](http://prototypejs.org/) [[GitHub]](https://github.com/sstephenson/prototype/)
    - [Zepto](http://zeptojs.com/) [[GitHub]](https://github.com/madrobby/zepto/)
    - [MooTool](http://mootools.net/) [[GitHub]](https://github.com/mootools/mootools-core/)

  - 模块化
    - ES6 Module
    - CommonJS

  - 框架  
    - [AngularJS](https://angularjs.org/) [[GitHub]](https://github.com/angular/angular.js/)
    - [Backbone](http://backbonejs.org/) [[GitHub]](https://github.com/jashkenas/backbone/)
    - [Knockout](http://knockoutjs.com/) [[GitHub]](https://github.com/SteveSanderson/knockout/)
    - [Ember](http://emberjs.com/) [[GitHub]](https://github.com/emberjs/ember.js/)
    - [React](http://facebook.github.io/react/) [[GitHub]](https://github.com/facebook/react/)
    - [polymer](https://www.polymer-project.org/) [[GitHub]](https://github.com/polymer/polymer/)
    - [Deft.js](http://deftjs.org/) [[GitHub]](https://github.com/deftjs/DeftJS/)
    - [Vue](http://vuejs.org/) [[GitHub]](https://github.com/yyx990803/vue/)
    - [Riot](http://riotjs.com/) [[GitHub]](https://github.com/riot/riot)
  
  - UI框架
    - [Bootstrap](http://getbootstrap.com/) [[GitHub]](https://github.com/twbs/bootstrap/)
    - [Semantic UI](http://semantic-ui.com/) [[GitHub]](https://github.com/Semantic-Org/Semantic-UI/)
    - [Foundation](http://foundation.zurb.com/) [[GitHub]](https://github.com/zurb/foundation/)
    - [Material UI](http://material-ui.com/) [[GitHub]](https://github.com/callemall/material-ui/)
    - [WinJS](https://dev.windows.com/en-us/develop/winjs) [[GitHub]](https://github.com/winjs/winjs)
    - [Pure](http://purecss.io/) [[GitHub]](https://github.com/yahoo/pure/)
    - [Amaze UI](http://amazeui.org/) [[GitHub]](https://github.com/allmobilize/amazeui)
  
  - WebSocket
    - [Socket.io](http://socket.io/) [[GitHub]](https://github.com/Automattic/socket.io/)
    - web-socket-js [[GitHub]](https://github.com/gimite/web-socket-js/)

  - WebGL
    - [Three.js](http://threejs.org/) [[GitHub]](https://github.com/mrdoob/three.js/)
    - [Babylon.js](http://www.babylonjs.com/) [[GitHub]](https://github.com/BabylonJS/Babylon.js/)
    - [Pixi.js](http://www.pixijs.com/) [[GitHub]](https://github.com/GoodBoyDigital/pixi.js/)
  
  - CSS3 动画
    - [Animate.css](https://daneden.github.io/animate.css/) [[GitHub]](https://github.com/daneden/animate.css/)
    - [bounce.js](http://bouncejs.com/) [[GitHub]](https://github.com/tictail/bounce.js/)
    - [Effeckt.css](https://h5bp.github.io/Effeckt.css/) [[GitHub]](https://github.com/h5bp/Effeckt.css/)
    - [move.js](https://visionmedia.github.io/move.js/) [[GitHub]](https://github.com/visionmedia/move.js/)
  
  - 流程控制
    - ES6
      - Promise
      - Generator
    - ES7
      - yield
      - await
      - async [[GitHub]](https://github.com/caolan/async/)
      - co [[GitHub]](https://github.com/tj/co/)
    - Promise
      - Bluebird [[GitHub]](https://github.com/petkaantonov/bluebird/)
      - q [[GitHub]](https://github.com/kriskowal/q/)
      - when.js [[GitHub]](https://github.com/cujojs/when/)

- 转义标准
  - [babel](https://babeljs.io/) [[GitHub]](https://github.com/babel/babel)

- 模板引擎
  - [Handlebars](http://handlebarsjs.com/) [[GitHub]](https://github.com/wycats/handlebars.js/)
  - [Haml](http://haml.info/) [[GitHub]](https://github.com/haml/haml/)
  - [Slim](http://slim-lang.com/) [[GitHub]](https://github.com/slim-template/slim/)
  - [Jade](http://jade-lang.com/) [[GitHub]](https://github.com/jadejs/jade/)
  - [Ejs](http://www.embeddedjs.com/)
  - [Spacebars](http://meteorcapture.com/spacebars/)
  - [mustache](http://mustache.github.io/) [[GitHub]](https://github.com/janl/mustache.js/)

- 中间语言
  - [TypeScript](http://www.typescriptlang.org/) [[GitHub]](https://github.com/Microsoft/TypeScript/)

## 6 可行性技术选型

- 选择一个框架（不采用，但请私下了解下）
  - Vue.js（大家都说好，那肯定不赖）

- 构建
  - NPM
  - Webpack
  - Babel
  - ESLint

- 选一个编辑器或ide：
  - Visual Studio Code

- 编码规范
  - es6
  - ts

- 数据加密
  - [crypto-js](https://github.com/brix/crypto-js)
    - 支持算法 MD5、SHA-1、SHA-256、AES、Rabbit、MARC4、HMAC、HMAC-MD5、HMAC-SHA1、HMAC-SHA256、PBKDF2、

- 代码保护
  - [uglify](http://lisperator.net/uglifyjs/transform)
    - 储蓄安全，js代码需自行实现混淆算法，**破解者只要有耐心**，没得办法。
  - [小程序插件机制](https://developers.weixin.qq.com/miniprogram/dev/framework/plugin/)
    - 第三方小程序在使用插件时，也无法看到插件的代码。

## 7 尾声：安利林哥

![talk is cheap ](/webar/doc/linus01.jpeg)

前端发展迅速，目前仍属于快速发展变更频繁阶段，没有一个框架能够解决所有的问题，然而

- 约定多了会令我们会丧失思考能力
- 框架多了会让我们丧失动手能力

共勉：作为程序员请时刻保持清醒，满足业务需求同时跟进时代发展创造下一个奇迹的，可能是你。

![talk is cheap ](/webar/doc/linus-fuck-nvidia.jpg)

[link-wiki]:https://en.wikipedia.org/
[link-Front_and_back_ends]:https://en.wikipedia.org/wiki/Front_and_back_ends
[link-Front-end_web_development]:https://en.wikipedia.org/wiki/Front-end_web_development
[link-Web_application]:https://en.wikipedia.org/wiki/Web_application
[link-WWW]:https://en.wikipedia.org/wiki/World_Wide_Web
[link-W3C]:https://en.wikipedia.org/wiki/World_Wide_Web_Consortium
[link-html5]:https://en.wikipedia.org/wiki/HTML5
[link-CSS]:https://en.wikipedia.org/wiki/Cascading_Style_Sheets
[link-html]:https://zh.wikipedia.org/wiki/HTML
[link-js]:https://en.wikipedia.org/wiki/JavaScript
[link-ECMAScript]:https://en.wikipedia.org/wiki/ECMAScript
[link-sun]:https://en.wikipedia.org/wiki/Sun_Microsystems
[link-Netscape]:https://en.wikipedia.org/wiki/Netscape
[link-Nexus]:https://en.wikipedia.org/wiki/WorldWideWeb
[link-Web_browser]:https://en.wikipedia.org/wiki/Web_browser
[link-Netscape_Navigator]:https://en.wikipedia.org/wiki/Netscape_Navigator
[link-Mosaic]:https://en.wikipedia.org/wiki/Mosaic_(web_browser)
[link-Opera]:https://en.wikipedia.org/wiki/Opera_(web_browser)
[link-Internet_Explorer]:https://en.wikipedia.org/wiki/Internet_Explorer
[link-Browser_wars]:https://en.wikipedia.org/wiki/Browser_wars
[link-Safari]:https://en.wikipedia.org/wiki/Safari_(web_browser)
[link-Mozilla_Application_Suite]:https://en.wikipedia.org/wiki/Mozilla_Application_Suite
[link-Firefox]:https://en.wikipedia.org/wiki/Firefox
[link-Firefox#History]:https://en.wikipedia.org/wiki/Firefox#History
[link-KHTML]:https://en.wikipedia.org/wiki/KHTML
[link-Google_Chrome]:https://en.wikipedia.org/wiki/Google_Chrome
[link-Microsoft_Edge]:https://en.wikipedia.org/wiki/Microsoft_Edge
[link-WebKit]:https://en.wikipedia.org/wiki/WebKit
[link-V8]:https://en.wikipedia.org/wiki/V8_(JavaScript_engine)
[link-V8-org]: https://chromium.googlesource.com/v8/v8.git
[link-JavaScriptCore]:https://en.wikipedia.org/wiki/WebKit#JavaScriptCore
[link-Chakra]:https://en.wikipedia.org/wiki/Chakra_(JavaScript_engine)
[link-chromium]:https://www.chromium.org/
[link-blink]:https://www.chromium.org/blink
[link-Comparison_of_web_browsers]:https://en.wikipedia.org/wiki/Comparison_of_web_browsers
[link-SpiderMonkey]:https://en.wikipedia.org/wiki/SpiderMonkey
[link-Rhino]:https://zh.wikipedia.org/wiki/Rhino_(JavaScript%E5%BC%95%E6%93%8E)
[how-javascript-works-inside-the-v8]:https://blog.sessionstack.com/how-javascript-works-inside-the-v8-engine-5-tips-on-how-to-write-optimized-code-ac089e62b12e
[link-mdn]:https://developer.mozilla.org/zh-CN/docs/Web
[link-statcounter_all]:https://gs.statcounter.com/browser-market-share  
[link-statcounter_chaina]:https://gs.statcounter.com/browser-market-share/all/china  
[ref-01]:https://developers.google.com/web/updates/2018/09/inside-browser-part1
[ref-02]:https://developers.google.com/web/updates/2018/09/inside-browser-part2
[ref-03]:https://developers.google.com/web/updates/2018/09/inside-browser-part3
[ref-04]:https://developers.google.com/web/updates/2018/09/inside-browser-part4
[link-pwa]:https://lavas.baidu.com/pwa/README
[link-ts]:https://www.tslang.cn/samples/index.html
