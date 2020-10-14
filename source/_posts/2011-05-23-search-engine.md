---
id: 710
title: 搜索引擎
date: 2011-05-23T18:06:08+00:00
author: tanglei
layout: post
guid: http://www.tanglei.name/?p=710
duoshuo_thread_id:
  - 1351844048792453293
categories:
  - 课程学习
tags:
  - 电子商务
---
**一、 搜索引擎定义**
  
搜索引擎(Search Engine)是指根据一定的策略、运用特定的计算机程序收集互联网上的信息，在对信息进行组织和处理后，并将处理后的信息显示给用户，是为用户提供检索服务的系统。
  
**二、 **搜索引擎******分类** ****
  
1)         全文搜索引擎——名副其实的搜索引擎，它们从互联网**提取**各个网站的信息（以网页文字为主），**建立**起数据库，并能**检索**与用户查询条件相匹配的记录，按一定的**排列**顺序返回结果。搜索结果来源的不同，全文搜索引擎可分为两类：
  
i.     拥有自己的网页抓取、索引、检索系统（Indexer），能自建网页数据库，搜索结果直接从自身的数据库中调用。Google和百度就属于此类；
  
ii.     租用其他搜索引擎的数据库，并按自定的格式排列搜索结果，如Lycos搜索引擎。
  
l  自动信息搜集功能有两种：定期搜索+提交网站搜索
  
l  特点是搜全率比较高。
  
2)         目录索引——将网站分门别类地存放在相应的目录中。严格意义上不能称为真正的搜索引擎，只是按目录分类的网站链接列表而已。用户完全可以按照分类目录找到所需要的信息，不依靠关键词（Keywords）进行查询。目录索引中最具代表性的是Yahoo、新浪分类目录搜索。
  
l  特点是查找的准确率比较高。

3)         元搜索引擎（Meta Search Engine）——接受用户查询请求后，同时在多个搜索引擎上搜索，并将结果返回给用户。InfoSpace、Dogpile、Vivisimo(自定的规则将结果重新排列组合)等，中文的搜星(曾经)。

4)         垂直搜索引擎——专注于特定的搜索领域和搜索需求(旅游、机票etc)，在其特定的搜索领域有更好的用户体验。相比通用搜索动辄数千台检索服务器，垂直搜索需要的硬件成本低、用户需求特定、查询的方式多样。Eg:搜驴(chinaevery.com)

**三、**搜索引擎******工作原理** **[<img class="aligncenter size-full wp-image-711" title="search-engine" src="/wp-content/uploads/2011/05/search-engine.jpg" alt="搜索引擎"  />](/wp-content/uploads/2011/05/search-engine.jpg)**
  
1)         抓取网页：Spider/Crawler/Robot顺着网页中的超链接，连续地抓取网页，被抓取的网页被称之为网页快照。
  
2)         处理网页:最重要的就是提取关键词，建立索引文件，其他还包括去除重复网页、分词（中文）、判断网页类型、分析超链接、计算网页的重要度/丰富度等。
  
3)         提供检索服务:搜索引擎从索引数据库中找到匹配用户输入关键词的网页

l  核心算法: 网页抓取程序（网络蜘蛛）、关键词提取、索引文件创建方式、重复网页合并、结果排序算法、中文分词算法（如：理念**和服**务）、网页类型判断（语言判断：meta标签、字符编码、内容分析等）、超链接分析、网页重要性与丰富度计算

四、**搜索引擎****组成部分：**搜索器、索引器、检索器和用户接口
  
1)         搜索器：其功能是在互联网中漫游，发现和搜集信息；两种策略：
  
i.     从一个起始URL集合开始，顺着这些URL中的超链接（Hyperlink），以宽度优先、深度优先或启发式方式循环地在互联网中发现信息。
  
ii.     将Web空间按照域名、IP地址或国家域名划分，每个搜索器负责一个子空间的穷尽搜索。

2)         索引器：其功能是理解搜索器所搜索到的信息，从中抽取出索引项，用于表示文档以及生成文档库的索引表；索引技术是搜索引擎的核心。索引项有两种：
  
i.     客观索引项：与文档的语意内容无关，如作者名、URL、更新时间、编码、长度、链接流行度（Link Popularity）等等；
  
ii.     内容索引项：反映文档内容的，如关键词及其权重、短语、单词等等。内容索引项可以分为单索引项和多索引项（或称短语索引项）。

索引数据表和信息数据表是两个独立的表，只是索引数据表和信息数据表是一对多的关系，这样或许更好理解。搜索引擎就迫切希望将用户查询的信息锁定在一个范围，这个范围的信息量或许只有几千条、几百条，计算处理起来，效率比直接到信息数据表查询要高很多，索引数据表就是为解决这一问题出现的。
  
索引表一般使用某种形式的倒排表（Inversion List），即由索引项查找相应的URL或文档。索引表也要记录索引项在文档中出现的位置，以便检索器计算索引项之间的相邻关系或接近关系，并以特定的数据结构存储在硬盘上。

3)         检索器：其功能是根据用户的查询在索引库中快速检索文档，进行相关度评价，对将要输出的结果排序，并能按用户的查询需求合理反馈信息；常用的信息检索模型有集合理论模型、代数模型、概率模型和混合模型四种。

4)         用户接口(HTML页面)：其作用是接纳用户查询、显示查询结果、提供个性化查询项。用户接口的设计和实现使用人机交互的理论和方法，以充分适应人类的思维习惯。可以分为简单接口和复杂接口两种：
  
i.     简单接口——只提供用户输入查询串的文本框；
  
ii.     复杂接口——让用户对查询进行限制，如逻辑运算（与、或、非）、相近关系（相邻、NEAR）、域名范围（如.edu、.com）等等。

**五、** **网络蜘蛛基本原理** ****
  
网络蜘蛛即Web Spider是通过网页的链接地址来寻找网页，从网站某一个页面（通常是首页）开始，读取网页的内容，找到在网页中的其它链接地址，然后通过这些链接地址寻找下一个网页，这样一直循环下去，直到把这个网站所有的网页都抓取完为止。一种半自动的程序，因为它总是需要一个初始链接（出发点），随后就自动了。评价网页重要性的主要依据之一是某个网页的链接深度。两种抓取策略广度优先和深度优先：
  
1)         广度优先：指网络蜘蛛会先抓取起始网页中链接的所有网页，然后再选择其中的一个链接网页，继续抓取在此网页中链接的所有网页。这是最常用的方式，因为这个方法可以让网络蜘蛛并行处理，提高其抓取速度。
  
2)         深度优先是指网络蜘蛛会从起始页开始，一个链接一个链接跟踪下去，处理完这条线路之后再转入下一个起始页，继续跟踪链接。这个方法有个优点是网络蜘蛛在设计的时候比较容易。
  
l  关键问题：
  
1)         HTML分析：需要某种HTML解析器来分析蜘蛛程序遇到的每一个页面。
  
2)         页面处理：需要处理每一个下载得到的页面。下载得到的内容可能要保存到磁盘，或者进一步分析处理。
  
3)         多线程：只有拥有多线程能力，蜘蛛程序才能真正做到高效。
  
4)         确定何时完成：不要小看这个问题，确定任务是否已经完成并不简单，尤其是在多线程环境下。