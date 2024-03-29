---
layout: post
title: "53期 - Ubuntu的商业&教育用途 - 第2部分"
date: 2012-04-26 20:13
comments: true
categories: issue53 HOW-TO
---

`作者：Jess Avilés 翻译：刘丹阳 校对：吴云 梁远金`

从上期杂志起，我开始讨论家庭办公或小型商业环境中运行于Ubuntu系统的软件需求。为提供一个参考起始点，我描述了一个五人公司的虚构环境，存在台式机与笔记本混用的情况，以及部分硬件要求。现在我们已经完成了硬件的部署，接下来就该转到满足我们需求而必备的软件上来了。商业应用将运行在Ubuntu10.04中，因为长期发行版系统具有一个已知的长期支持。为了明确公司的需求，让我们先来评估一下工作流程。这是一个含义宽泛的词，意为“为达到目标而需完成的步骤”。看看本杂志的第二页吧。你会看到LibreOffice、GIMP、Scribus与Creative Commons的标志。LibreOffice是用于管理文章中的文本。GIMP用于照片的缩放与润饰，而Scribus则用于文本、图片、流程以及pdf生成管理。Creative Commons则为所得的作品提供许可。

工作流程可以被非常广义或狭义地定义。我们会广义地定义工作流程如下： 

1. 针对潜在客户调整公司市场策略。
2. 客户呼叫，传递项目详细信息，同时寻求方案提议（成本估算）。
3. 方案提议经过研究与提炼，然后通过邮件发送出去。
4. 客户接受方案提议。初始文书工作完成。
5. 调研工作展开。收集样品与照片，撰写调查记录与绘图。样品递送至实验室。
6. 评估实验室报告与调查记录，缩放图片，撰写并发送报告给客户。
7. 进行发票开具与收款（自客户与承包商）。
8. 记录归档。

<!--more-->

从这个工作流程可以看到我们需要如下类型的软件：

- 桌面与基于web的发布功能（工作流程1）
- 办公效率（工作流程3与6）
- 邮件与联系人管理（工作流程1、2、3、4、6与7）
- 会计（工作流程4、5与7） 
- 图片处理、CAD、GIS与扫描（工作流程1、5、6、7与8）
- 记录管理（工作流程3、4、6、7与8）

鉴于所需软件已明晰，首个检索的位置是Ubuntu的软件仓库，然后是网络。软件可以是开源的，然后可能不产生费用，但也可能会是商业软件。记住一个free（你可以随意理解）的选择并非一定存在。如果软件不在资源库中，那么它应该被打包成deb包，并且尽可能少的需要外部依赖。你也可以查看Ubuntu列表中那些[已通过认证的软件](http://webapps.ubuntu.com/partners/certified-software/)，以寻找适用的软件。这些说明有助于将所遇到的问题最小化。

### 桌面与基于网络的发布功能

传单、商业卡片、宣传册以及网页均属此范畴。当你会访别人的时候，双方会交换名片。如果你在参加一个工业展或者一个潜在客户的会议，应该随身带上宣传册与传单。所有这些东西都附有联系信息、邮箱地址与网址。

如果你有用过 MS Publisher、Adobe Frame Maker或者Quark Express，你会知道印刷出版物中元素在页面上的准确定位是必须条件。在Ubuntu上，你可以使用 [Scribus](http://www.scribus.ne)。Scribus是一个桌面排版软件（DPS）。其准确定位与色彩管理特性使其成为最佳的自由与开源DPS工具之一。Scribus与常规DPS工具一样，均非文本处理器。放松心情去学习Scribus吧。你可以查看FullCircle前八期的杂志，上面有其教程。一旦掌握了使用的窍门儿，你的纸质出版物印出来之后将是你看到过最棒的。

Scribus在创建调研过程中收集数据的表格方面也很有用。如果你想把表格带到专业的打印店去打印，使用Scribus可以直接导出pdf。关于pdf，存在一个问题就是如果你尝试从pdf中提取文本，提取结果可能就不是那么的让人赏心悦目了。所提取的文本字间可能会有空格，并且每一行都是独立的新行。用Writer将一页有几个段落的页面导出为pdf，然后用Scribus进行相同的操作。你就会明白我的意思了。Scribus也是一款创建pdf表单的优秀工具。其主要缺点在于行与行之间的多行框中存在过大的空隙，这使其看起来很难看。还有，它没有让用户保存填入内容后的pdf选项。Scribus同样可以使用矢量图（[Inkscape](http://inkscape.org)） 与点阵图 （[GIMP](http://www.gimp.org)）。你可以用Inkscape来创建你公司的标志以及各种剪贴画。将标志创建成矢量图有个优势，那就是你可以在不损失分辨率的情况下放大图片。

<!--more-->

基于web的发布是另一回事。 MS Publisher 可以将你的文档转换为网页。完成这样的操作也许没问题，但产生的代码会很可怕，且是为IE黑客们量身定做的。软件仓库里有 [Bluefish](http://bluefish.openoffice.nl/index.html) 与 ([Kompozer](http://www.kompozer.net))。两者均为网页编辑工具，但是Bluefish仅适用于手工编程人员。有了这两款软件，你就可以创建html、PHP、javascript或者之中的任意组合。Bluefish的开发很活跃，而Kompozer相对就缓慢了。如果你打算采取这种方式，确保你用上一个严谨的DTD（Document Type Definition ，文件类型定义），同时别再惦记表格排版的事儿了。严谨的DTD html与CSS布局会给你带来最少的头疼事儿，因为你在遵循一个严谨的秘诀——展示是通过CSS进行控制，然后信息通过html标记进行控制。当厌倦了你网站的外观时，你只需修改CSS即可。当需要更新信息时，找到html源文件就可以进行了。在不同的浏览器中，你的网页看起来并非一定会完全一样，即使你用上了黑客技术也无法保证其会一成不变。同样，如果你稍后雇人管理你的网站，那么一个严格的DTD也会易于让不同的人对其进行维护与读码。

也请记住有许多人是通过智能手机访问互联网的，而某些人则会需要打印你的信息。为这两类人分别提供一个界面、打印与移动版CSS规则会是一个好点子。记住每种媒介都是独特的，你无需令其看起来一模一样。打开Firefox浏览器的首选项，然后查看内容标签。“字体&颜色”部分的高级选项会显示出用于网页的字体大小与字体，而网页自身是不会为字体显示提供任何特殊规则的。如果你没有改过设置，字体会显示为serif，大小会显示为16磅。如果你以打印预览形式打开同一个网页，字体可能会过大。一条CSS规则可能会让屏幕字体保持在1em（译注：em，西文排版行长单位），但是会设置其打印字体大小为12磅。一条移动版规则也许就能让字体保持一致，但会默认隐藏所有图片，或者使用备选的小图片。这样，你的网页就可以自动为不同的用户服务，而无需你去做任何特殊的java或者ajax magic处理。

另一个你可以使用的工具是 [Drupal](http://www.drupal.org)。Drupal 提供了几个模板，并且会为你处理所有的编码工作。有些托管公司会为其客户提供一个Drupal设置选项。你只需添加你的文本内容到Drupal提供的模板即可。访问 [http://drupal.org/hosting](http://drupal.org/hosting) 寻找适合你的托管服务吧。

### 办公效率

这是为大多数人所熟知的软件集合。Ubuntu提供了OpenOffice作为默认的办公效率套件。OpenOffice与MS Office足够类似，所以大部分人只需极少的培训就能适应其使用。使用OpenOffice的好处包括可以打开MS Office文档，拥有一套全功能办公效率应用。你不单拥有了文字处理器、电子表格以及演示软件，通过绘图套件你还拥有了流程图与图表，并且还有Base套件的数据库应用（这个不在Ubuntu默认安装的范围内）。如需完整套件，请打开软件中心，然后下载OpenOffice.org的Office套件，或者只安装OpenOffice.org的Base套件来获得数据库应用。完整安装会带给你某些传统功能与移动设备滤镜。

因为OpenOffice可与MS Office相媲美，所以你对其不应有任何的疑虑。需要记住的一件事是：OpenOffice是用于创建“开放文档格式（odf）”文档的工具，就像微MS Office是创建Office OpenXML文档的工具一样。虽然各自的套件都支持打开对方的文件格式，它们依然最适合处理由自己创建的文件。简而言之，使用ODF作为你默认文件格式就对了。

使用一个免费套件就意味着你得不到一些东西，诸如：模板、剪贴画与语法查错器，但是这些都可以通过下载获取到。最棘手的一个是语法工具。你得去 [Lingucomponent](http://lingucomponent.openoffice.org/grammar.html) 的网页寻找能用的工具。After the deadline （http://afterthedeadline.com）在已有的工具中是最棒的，而不足之处在于你需要将其安装到你的服务器上，且要求服务器至少配备4G内存与多个核心。想用就得掏腰包咯。

OpenOffice为用户提供了使用指南，[地址](http://wiki.services.openoffice.org/wiki/Documentation/OOo3_User_Guides)。将其下载下来，以供你的员工使用。他们首次使用此办公套件以及进行迁移时遇到的许多难点在指南里都有解释说明。对于Writer而言，应该历遍段落的概念与页面格式，因为这些东西曾经让我吃尽了苦头。学习使用段落、字符以及页面风格，因为这些都相当实用。还是孩提时候，我们就被反复教导要侧重于文本本身，而文字处理器惯成了我们在使用粗体与斜体时的坏习惯。同样的事情还发生在分段过程中，我们习惯于添加一个无内容的空白段落而非使用类似于文本主体的段落样式。

Calc提供了具有数学公式与图表功能的电子表格。当你有一个包含需要与标准值相比较值的表格时，这种条件格式就可以大派用场了。一旦完成设定，符合你要求的数据将会被自动格式化。我将规则格式应用于大于参考标准的值，包括粗体、下划线、斜体或者其中的任意组合。这些数值随后会被绘制成图表以进行评估，例如，观察其随时间或空间改变而变化的趋势。Calc的公式还为统计学、逻辑学、算法以及金融需求提供了广泛的覆盖面。

许多Impress用户会抱怨其缺乏模板，且这类抱怨还在继续着。Impress在完成其工作方面已经做得足够好了。Transitions很不错，而且我发现一点嵌入式媒体播放器比Powerpoint工作得更好。Impress可以自动播放影片，而用Powerpoint就做不到这点。

捆绑的office套件可提供你所需要的东西。不过，还有LibreOffice这么个选择。目前LibreOffice预置于当前版本的Ubuntu，且看起来在下一个LTS版本（12.04）中它会内置。对于LibreOffice，我对所言持保留意见。因为LibreOffice某些特性还无法与OpenOffice相媲美。不过如果你打算用一下，在 [https://wiki.ubuntu.com/LibreOffice](https://wiki.ubuntu.com/LibreOffice) 上照着指令安装即可。而由于两者不能并存，你必须要卸载OpenOffice。

Lyx是一个你可以试试的备选文档处理器。作为Latex的前端，Lyx强调的是写作；Latex规则被用于格式化文档。基本文本类很不错，然而习惯于管理每一个空格的人则可能会觉得它们令人沮丧。Lyx摒弃了Latex的一些复杂特性，而那些了解Latex的人则可以创建新文本类以满足他们的需要。Lyx可以输出pdf、html、DVI以及其他的文件。

邮件与联系人管理 Evolution——了解它，爱上它吧。它与MS Outlook或IBM的 Lotus Notes没什么不同。用它可以管理你的电子邮件，联系人还有日历。简单连接到你的地址簿，然后你就可以轻松地进行邮件合并工作了。

会计 这是一个带有挑战的范畴——因为没有多少适用于Linux小型商业环境的免费会计软件包。幸运地是，软件仓库有个Canonical Partner源可以链接到相关软件。Openbravo ERP是一个基于web的应用，付费后你可以用它来管理工程、开具发票以及访问商务智能工具。已认证软件页面也还链向了[Accountz](http://www.accountz.com)) 和 [Muli](http://www.muli.com.au) 。虽然我对这些软件包没有任何使用经验，但是Ubuntu认为其可以正常使用。而它们能否做成你要求的东西则是另一回事了。

### 图片处理、CAD、GIS与扫描

数字化维护调研过程中拍摄的照片、手工绘图与样品地理定位等所有东西需要使用特殊的软件。让我们开始看看图片处理软件吧。如果你是Ubuntu新手，那么可能不知道GIMP的存在了，因为它不再是默认预置的应用了。到软件中心把它下载下来吧。GIMP常被拿来与PhotoShop做比较，因其与后者同样的强大 。如果你细心地学习其使用，就可以对你的图片做很多处理了。它会是你桌面与web发布应用的工作流程的组成部分。在这个实例中，我们更多地是用它来调整图片大小，因为它给了我们使用物理单位（毫米或英寸）的选项。当图片作为报告组成部分被打印出来的时候，它们只会占用一整块空间，如一个4×6英寸的面积。如果用当下常见的相机进行全分辨率拍照的话，那么大部分情况下你会得到一张大小在30英寸范围内而容量为几兆的图片。如果你要用几张这样的图片来创建一个文档（假如是用Draw），那么生成的文件将会臃肿笨重且打印起来速度缓慢。用GIMP打开图片，然后找到图片（Image）菜单。从那儿选择缩放（Scale）。在对话框中选择分辨率，确保x和y之间的链节（chain link）没被取消掉，如果它不是300，将其改为300。看看尺寸是怎样改变的。现在转到单位选择框并选择英寸。图片通常会被美化——意味着宽度是最大的尺寸。改变尺寸至4英寸，然后高度将随之自动改变。以别名另存此图，然后比较其与源文件的大小。使用这些缩放后的图片会让你拥有一份极佳的打印文档，且文件大小也成为可控的。

Ubuntu默认的扫描应用是Simple Scan，它确实简单。你可以扫描从第三方接收的文档，Simple Scan预置支持A4、A5、A6、信件、法定尺寸以及4×6大小。分辨率被限制为几个选项，保存选项也仅限于pdf、jpg与png格式。虽然我觉得这些设置已经足够了，但是Simple Scan总是扫描得到最大尺寸的图片，然后我不得不单独处理每张图片。在使用文档进纸器时， Simple Scan可以检测到最后的页面然后停止扫描。Simple Scan不支持使用带纸张自动整理功能的文档进纸器进行双面扫描。 Simple Scan同样缺失光学文字识别（OCR，optical character recognition）选项，因为那不属于其目标。

对于OCR和一些更多的高级特性，可以看看 [gscan2pdf](http://gscan2pdf.sourceforge.net)。Gscan2pdf是一个不同工具的集合，它使目前的扫描变得更为方便。其功能之一就是通过 [unpaper](http://unpaper.berlios.de) 进行页面清洁与页面纠偏。通过使用 [scanadf](http://www.martoneconsulting.com/sane-scanadf.html)，gscan2pdf在当一个ADF超出页面后gscan2pdf就会应该检测得到异常。遗憾的是，在我这儿这个特性不起作用了。我用的是HP惠普的Photosmart Premium并且，每次用ADF时我都必须输入打印页数到机器里。要使用OCR，你得先安装一个OCRC引擎。当然我有，因为在我用过的引擎里，有Tesseract （http://code.google.com/p/tesseract-ocr）我才得到了满意的结果。在安装gscan2pdf之前，先安装这个软件并选择你需要的语言版本。我在Uubuntu上使用过的工具没有一个与在Wwindows上用的是相似的工作方式。我将多功能打印机与软件捆绑，可以扫描文件为pdf，且可以通过拉线选择的方式复制文本与插入OCR识别所得的文本。这样只要选择复制文本的行数就可以扫描pdf和插入OCR'd文本。当保存文档为pdf格式时，gscan2pdf会将OCR识别的'd文本放进备注里，里面会有一些琐碎的东西而这会让某些人觉得有点奇怪。我将此视为软件目前状态的一种不足限制。另一个不足限制是复杂的的排版布局分析。Ocropus（http://code.google.com/p/ocropus ）和Cuneiform （http://launchpad.net/cuneiform-linux）是配合gscan2pdf使用的备选OCR与排版分析引擎。你的结果将依随于文档的布局排版方式而改变，还有，这两个工具都只能在命令行下使用。

一旦完成了调研绘图的扫描，你就得要使用CAD程序对其他们进行数字化处理。对于那些只知道AutoCAD的人而言来说，Uubuntu中的应用选择项会让你惊喜。AutoCAD是不免费的，而软件仓库中的最佳选择是QCAD。QCAD分免费版与收费版（www.qcad.org）的。商业版仅需$36.00并且很值得拥有，性价比极高。我用商业版的原因是为了获得pdf的导出功能。商业版除了拥有bug修复外还具有某些新特性。我用QCAD制作设备布局图，工具以及标记有用的东西。它具有一个模型空间而无纸质空间。于我而言，缺少纸质空间是其最主要的不足，但我已经学会习了如何绕过它去干活。它所用的默认文件类型是dxf，而且不支持AutoCAD dwg格式的导出。对我来说这不成问题，但是如果你想要dwg支持，那么看看Bricsys吧，可以从 （http://www.bricsys.com）在那儿获得Bricsys。它在Ubuntu下工作得很好（属于一个Ubuntu软件合作伙伴），比QCAD要复杂得多，所以有个情理之中的价格$400。另一个免费的选择是DraftSight（ http://www.3ds.com/products/draftsight/free-cad-software/）。看起来它有足够好的前景——提供了类似Bricsys的功能。当我在Uubuntu中安装完之后，基本没法运行它。虽然我看到了硬件规格，但是移动鼠标和添加元素的时候，速度都慢得让人痛苦。这让我想起了有一次玩游戏的时候，我的显卡达不到最低要需求时的那种难受的感觉。几天前之后，新版本发布了——所以东西可能会有所改变。我会继续使用QCAD，因为它可以满足我的需求。

地理信息系统软件是工具箱的一个组成部分，被应用于环境科学与其他很多地方。它让我们可以评估许多不同区域之间的地理关系。如果你有一部个Android安卓手机，可以用谷歌纵横（Latitude）或地图（Maps）。如果得到了你当前的位置，你就可以看到你周围都有些什么。你是否想知道一所大学的存在对周边地区学风的影响？可以访问US Census的网页（http://www.census.gov/geo/www/tiger）， 并且下载他们的数据。接着获取几所当地大学的位置信息，并使用GIS工具以观察距离是否发生了改变。这就是地理信息的实际用途。GIS甚至被用于打击犯罪（http://gislounge.com/crime-mapping-gis-goes-mainstream/）。说到我对的GIS需求的话，我用的是QGIS（http://www.qgis.org），这个不在软件仓库中。你将需要按照说明（http://www.qgis.org/wiki/Download#Ubuntu）添加他们的软件仓库。安装它时还要装上GRASS插件。曾经使用过ArcGIS的人会发现QGIS有点儿眼熟。我发现其存在的主要问题与它附带着Coordinate Reference System坐标参考系统有关（一种给出位置占位符信息的本地定位信息系统）。阅读关于此类信息的手册，因为它运行起来与和ArcGIS还是稍有差别的。

在创建轮廓图时，QGIS也能派上用场，无论是根据高海拔还是污染浓度。可按照Scratching Surfaces上的教程去完成这些工作，地址为 [http://www.surfaces.co.il/?p=595](http://www.surfaces.co.il/?p=595) 和 [http://www.surfaces.co.il/?p=578](http://www.surfaces.co.il/?p=578)。

### 记录管理

有些时候人们会忘记那些所收集或创建而被管理了几年时间的信息。职业健康安全管理局 (OSHA，Occupational Health and Safety Agency)要求雇主在员工离职后的30年里留存其与健康监测相关的特定检测记录（参见29 CFR 1910.1020(d)(1)(i) ）（二校注：CFR美国联邦法规全书）。美国环境保护局（EPA，US Environmental Protection Agency）有一个记录计划（http://www.epa.gov/records/policy/schedule/）用以他们的记录维护。记录（——无论是纸质的、电子的抑或者是其他的媒介的）都耗费着空间、金钱与时间。而这就是记录管理（ http://en.wikipedia.org/wiki/Records_management）。如果回到我们的工作流程中来，就会发现每一步都会产生记录：当提案建议被发送或接受时，作为调研工作组成部分而创建的文档、发票、付款、从第三方接收的文档等等。当将记录打印出来，然后开始装进文件柜的时候，你就得弄清楚哪些东西应该放入。电子档记录开始填充你的硬盘，这就需要你增加更多的硬盘驱动器了。据我了解，有人超过十年没有删过任何商业邮件。而永久性保留记录并无多好的商业意义。你必须要删掉一些。国家档案与文件署（NARA，the National Archive and Records Agency）有一个面向联邦机构的架构，用以开发创建记录管理指导（[http://www.archives.gov/records-mgmt/policy/rm-framework.html](http://www.archives.gov/records-mgmt/policy/rm-framework.html)）。这里面甚至有用于可持续格式（[http://www.archives.gov/records-mgmt/initiatives/sustainable-faq.html](http://www.archives.gov/records-mgmt/initiatives/sustainable-faq.html)）与 pdf （http://www.archives.gov/records-mgmt/initiatives/pdf-records.html）的指导。国际标准化组织（ISO）还提供出售一个由两大部分组成的标准电子记录管理（[http://www.iso.org/iso/iso_catalogue/catalogue_tc/catalogue_detail.htm?csnumber=31908](http://www.iso.org/iso/iso_catalogue/catalogue_tc/catalogue_detail.htm?csnumber=31908)）。这个澳大利亚的网页（[http://www.records-management.com.au/information.shtml?standards-](http://www.records-management.com.au/information.shtml?standards-)）上有一个来自全球的记录相关准则与指导的综合列表。

既然现在我已说服扔掉了那些不需要的记录，那我就可以跟你讲有关记录管理软件（RMS）的东西了。RMS如同一个文档网关般工作。你可以使用RMS保存文档到仓库的地下室中，同时确保能在这里面访问文档。RMS会跟踪文档的改变以及谁曾经调出并编辑过文档。它同时还掌管着文件归档工作。Canonical Partners软件仓库中有一个由一家公司提供的名为Nuxeo的软件可供选择。Nuxeo有部分记录管理功能，同时它也提供内容管理特性。想想那些被加到合同里的“条款和条件（Terms and Conditions）”吧。而现在那里有一个供你考虑的自由（或免费）的选择了。

另一款你可以考虑的RMS，而且还是通过DoD 5015.02认证过的，是 [Alfresco](http://www.alfresco.com)。它那儿有一个免费的社区版。我们正在寻找一个RMS，这也是我现在正在做的，Alfresco会是竞争者之一。评价它的主要原因在于其可以连接到Documentum（企业内容管理软件中的一个巨头）。我还没用过这款软件，但如果你想尝试一下用它，请注意Linux社区版只适用于64位机。

如你所见，Ubuntu可以提供一个小型环保公司所需的所有工具软件。于公司而言，主要的成本在于购置硬件，配置网络与部署以及购买软件。上面我所提及的大多数软件都是免费的，并且都在软件仓库中，这可以减少一些与软件搜索相关的头痛事情。有了这么棒的免费环境就无需恐惧要花一大笔钱去开家店咯。