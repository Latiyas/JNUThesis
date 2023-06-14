JNUMasterThesis v2.0
==============================
暨南大学博硕士学位论文Overleaf模板
==============================

缘起
--------------------------------------------------------
又是一年毕业季，辛辛苦苦写好的论文怎么保证格式的排版标准规范一直是令人头疼的问题。
在学术研究过程中，大家都开始接触并习惯于使用LaTeX进行论文的排版，那么是否也可以借助这个工具撰写毕业论文呢？在暨南大学数据存储与集群计算实验室的Yongtao Zhou学长早已完成了博硕士学位论文LaTex模板，但因为时间久远，加之软件版本不断更替，使用较新的本地LaTeX编译生成PDF文件过程中出现了一些错误往往难以解决。
同时，因为笔者写作经验较浅，一开始接触的便是Overleaf，所以情感上更倾向于Overleaf。私以为Overleaf存在以下几点优势：a.简洁，高效，省去了配置环境的麻烦；b.可以多人在线，共同编辑同一个文档。因此萌发了将暨南大学博硕士学位论文模板迁移至Overleaf上的念头。
本项目的主要工作是将Yongtao Zhou学长的暨南大学博硕士学位论文LaTeX模板迁移至Overleaf，同时根据同学们的反馈对格式继续进行完善。原始项目见[JNUMasterThesis](https://github.com/ytZhou/JNUMasterThesis)，再次感谢Yongtao Zhou学长前期的大量工作。参考文献借鉴了Haixing Hu学长的模板，详情见[GBT7714-2005-BibTeX-Style](https://github.com/Haixing-Hu/GBT7714-2005-BibTeX-Style)，感谢Haixing Hu学长提供的支持。
本项目虽然侧重于在Overleaf上进行编译测试，但同样支持在本地Latex上的编译。本项目在Overleaf网站上的共享链接为[https://cn.overleaf.com/read/pwvngpvxfxdd](https://cn.overleaf.com/read/pwvngpvxfxdd)，愿意使用Overleaf平台的同学可以直接拷贝项目进行修改。

已修复问题
--------------------------------------------------------
2023.03.17更新
1. 修正了目录、章节的标题对齐问题。
2. 修正了参考文献引用问题。
3. 重新调整了项目的结构。（感谢Yaju Li同学的帮助）
4. 修正了图、表目录的指引线格式以及图、表注释格式。
5. 重新调整了字体大小与与段落间距，修正了图表目录名称。（感谢Zhenxin Wu同学的帮助）

2023.04.10更新
1. 对齐了左右页边距。（感谢Weizhen Xu同学的帮助）

2023.04.30更新
1. 增加了书签，方便PDF阅读。
2. 修正了目录中的章节名称。

2023.05.10更新
1. 完善了参考文献的格式问题。

运行环境
--------------------------------------------------------
1. 在线注册Overleaf账号，依次点击"New Project->Upload Project->Upload Zipped Project"将文件上传至服务器。
2. 进入Project，找到"Menu"选项，将"Settings->Compiler"修改成"XeLaTeX"，将"Settings->Main document"设置为"main.tex"，选择"main.tex"进行编译即可。
3. 项目默认在texlive2022版本下运行。如果运行异常，建议检查"Settings->TeX Live version"的设置。

源码目录结构
--------------------------------------------------------
1. 根目录: main.tex是主文件，".ttf"或".ttc"文件是需要用到的字体文件，"gbt7714-2005.bst"是参考文献格式文件。
2. bib目录：bib文件存放目录，目前内容是本人常用的论文。
3. chapter目录(根据需要引用章节，引用方式为"\include{需要引用的章节名称}"):
    > 1) Lib.tex：根据需要引入功能包。
    > 2) declaration.tex：第一页论文信息，第二页独创性声明、学位论文授权使用书。
    > 3) abstract.tex: 中英文摘要。
    > 4) chaps.tex: 正文章节引用(管理除了declaration, abstract, conclusion, paper以及acknowledgement以外的所有正文内容，根据需要添加chapX.tex)。
    > 5) chap1.tex: 第一章。
    > 6) chap2.tex: 第二章。
    > 7) conclusion.tex: 结论。
    > 8) papers.tex: 攻读学位期间发表的论文。
    > 9) acknowledgement.tex: 致谢。
4. images目录：图片存放目录。

参考文献格式说明
--------------------------------------------------------
严格遵循中国国家标准[《GB/T 7714-2005: 文后参考文献著录规则》][gbt7714-2005]
详细信息见该项目：[GBT7714-2005-BibTeX-Style](https://github.com/Haixing-Hu/GBT7714-2005-BibTeX-Style)

注意事项
--------------------------------------------------------
1. 由于overleaf需要在线编译，编译速度较慢。因此，撰写文稿时可以仅引用当前编辑的章节方便快速查看。暂未使用的章节可以先行注释，当需要阅读全文时再全部引用。正文章节的引用一般是放在chaps.tex中。
2. 版本更新方式：拷贝最新的项目文件，将编辑好的bib、chapter以及img目录下的文件更新到对应的文件夹下即可。
3. main.tex中已包含了许多项目的编译设置，建议将新增宏包的引用放在Lib.tex中，方便对项目进行管理。

论文撰写小技巧
--------------------------------------------------------
1. 超过3个作者以上的中文参看文献，部分作者需要省略为”等“，可以在bib引用中额外增加参数”language={zh}“进行修复。

Author
--------------------------------------------------------
Ming Li

Email: li-ming96@foxmail.com

****************************分界线****************************
****************************分界线****************************
****************************分界线****************************

JNUMasterThesis v1.0
==============================
暨南大学博硕士学位论文LaTex模板 v1.0
==============================

目前提供的功能
--------------------------------------------
1. 实现了暨大毕业论文要求规范
2. 定理、引理等的中文化
3. 算法环境的中文化，算法默认使用algorithm2e
4. 图表的中文化
5. 提供对bib的支持，省去文献管理的麻烦
6. 简单使用实例的书写
7. 图表目录

PS：目前已不维护，如果功能需要更新可以在该源码上自行修改即可

排版样式参考
-----------------------------------------------
由于缺乏正式的官方模板且标准不一，本模板制作过程中主要参考了《暨南大学研究生学位论文格式要求》和宋梁山师兄的毕业论文《重复数据删除技术的实现与优化》，并从梁山师兄的毕业论文中选取部分章节进行对比，排版效果与梁山师兄的一致。另外，也纠正了梁山师兄毕业论文中部分小的排版问题。

通过实际使用，该模板符合暨大硕士和博士毕业论文格式要求。符合暨南大学研究生院https://gs.jnu.edu.cn/2016/0419/c882a131006/page.htm上提供了格式要求。

模板信息
-------------------
本模板为非官方模板，请选择性使用，最终权利和解释权归原作者ytZhou和[数据存储与集群计算实验室](http://dsc.jnu.edu.cn)所有。

您可以随意修改本模板功能，请务必保留原作者信息，尊重他人劳动成果。

使用样列请参考源码包中的PDF，源码包不提供基本的LaTex入门教程。如果您在使用过程需要基本的LaTex入门，请参考LaTex手册或者下面列出的资料。PS：由于自己误操作造成的损失原作者概不负责和理会，强烈建议使用网盘实时同步所写的源代码，避免不必要的损失。

本模板制作过程参考了《一份不太简短的LaTexe介绍》《LaTexe用户手册》《用LaTex写漂亮的学位论文》。在此感谢以上作者辛勤的付出，包括其它网络资料的作者。

主要参考的链接如下:

1.  http://blog.sina.com.cn/s/articlelist_1578561911_0_1.
2.  http://kb.mit.edu/confluence/pages/viewpage.action?pageId=3907168
3.  http://blog.csdn.net/xyqzki/article/details/6934729

PS：如需生成word版本请自行使用pdf转word工具转换，建议使用Adobe Acrobat。

源码目录结构
--------------------------------------------------------
1. bib目录：bib文件存放目录，目前内容是本人常用的论文.
2. chapter目录:

    > 1) declaration.tex：第一页论文信息，第二页独创性声明、学位论文授权使用书.
    >
    > 2) abstract.tex: 中英文摘要. 
    >
    > 3) chap1.tex:第一章.
    >
    > 4) chap2.tex: 第二章.
    >
    > 5) conclusion.tex: 结论.
    >
    > 6) paperList.tex: 攻读学位期间发表的论文.
    >
    > 7) acknowledgement.tex: 致谢.
> 区块中使用列表
> 1. 第一项
> 2. 第二项
> + 第一项
> + 第二项
> + 第三项
3. img目录：图片存放目录.

运行环境
---------------------------
Win8, [ctex](http://www.ctex.org/HomePage) (2.9.2), WinEdt 7.0下编译生成成功。


编译生成步骤
----------------------------
LaTex->B->LaTex->LaTex->dvi/pdf

Bug及其他反馈信息
-----------------------------------------
如果您在使用过程发现任何的bug和有更好的建议，可以通过邮件联系我y.t.zhou@foxmail.com

更新日志
-----------------------
1. 2015年4月9日。第一个版本发布v0.0.1
2. 2015年4月15日。更新第一页内容，增加学位类型。参考链接：http://gs.jnu.edu.cn/detail.html?1000109/W_13542_148575
3. 2015年4月19日。修改页眉格式，正确的是正文页眉加“暨南大学硕士学位论文”，可参见《暨南大学研究生学位论文格式要求》的第三节“学位论文的编写要求”的第二条。感谢立锋师兄指出此问题！
4. 2016年4月7日。最后一次更新至v1.0版本。加入图表目录，更优方案是写成独立样式文件，但是个人精力有限，且目前已满足需求，因此不再更新和维护。

致谢
---------------------------
首先，感谢邓玉辉教授给我们提供了宽松的科研环境，最后感谢实验室及其班里其他同学的帮助和支持。
JUN DSC Lab: https://dsc.jnu.edu.cn/ 

感谢[龙舜](http://mint.jnu.edu.cn:81/shun/)教授指出本手册的错误，并推广！

最后感谢使用本模板的各位同学！

Author
-------------------
Yongtao Zhou

Email: y.t.zhou@foxmail.com
