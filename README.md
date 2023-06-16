JNUThesis
==============================
暨南大学博硕士学位论文Overleaf模板
==============================

缘起
--------------------------------------------------------
又是一年毕业季，辛辛苦苦写好的论文怎么保证格式的排版标准规范一直是令人头疼的问题。
在学术研究过程中，大家都开始接触并习惯于使用LaTeX进行论文的排版，那么是否也可以借助这个工具撰写毕业论文呢？暨南大学数据存储与集群计算实验室的Yongtao Zhou学长虽然已完成了博硕士学位论文LaTex模板，但因为时间久远，加之软件版本不断更替，使用较新的本地LaTeX编译生成PDF文件过程中出现了一些错误或警告没有解决。
同时，由于笔者论文写作经验较浅，一开始接触的便是Overleaf，所以情感上更倾向于在线版的Overleaf。私以为Overleaf存在以下几点优势：a.简洁，高效，省去了配置环境的麻烦；b.可以多人在线，共同编辑同一个文档。因此萌发了将暨南大学博硕士学位论文模板迁移至Overleaf上的念头。

本项目的主要工作是将Yongtao Zhou学长的暨南大学博硕士学位论文LaTeX模板迁移至Overleaf，同时根据同学们的反馈对格式继续进行完善。原始项目见[JNUMasterThesis](https://github.com/ytZhou/JNUMasterThesis)，再次感谢Yongtao Zhou学长前期的大量工作。参考文献借鉴了南京大学的Haixing Hu学长的项目，详情见[GBT7714-2005-BibTeX-Style](https://github.com/Haixing-Hu/GBT7714-2005-BibTeX-Style)，感谢Haixing Hu学长的工作。

本项目虽然侧重于在Overleaf上进行编译测试，但同样能够在本地Latex上的编译通过。由于精力有限，暂时没有余力对本地编译的所有问题一一解决，请有问题的同学自行百度解决。本项目在Overleaf网站上的共享链接为[https://cn.overleaf.com/read/pwvngpvxfxdd](https://cn.overleaf.com/read/pwvngpvxfxdd)，愿意使用Overleaf平台的同学可以直接拷贝项目进行修改。

已修复问题
--------------------------------------------------------
2023.05.10更新
1. 完善了参考文献的格式问题。（感谢Yaju Li同学的帮助）

2023.04.30更新
1. 增加了书签，方便PDF阅读。
2. 修正了目录中的章节名称。

2023.04.10更新
1. 对齐了左右页边距。（感谢Weizhen Xu同学的帮助）

2023.03.17更新
1. 修正了目录、章节的标题对齐问题。
2. 修正了参考文献引用问题。
3. 重新调整了项目的结构。（感谢Yaju Li同学的帮助）
4. 修正了图、表目录的指引线格式以及图、表注释格式。
5. 重新调整了字体大小与与段落间距，修正了图表目录名称。（感谢Zhenxin Wu同学的帮助）

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
    > + Lib.tex：根据需要引入功能包。
    > + declaration.tex：第一页论文信息，第二页独创性声明、学位论文授权使用书。
    > + abstract.tex: 中英文摘要。
    > + chaps.tex: 正文章节引用(管理除了declaration, abstract, conclusion, paper以及acknowledgement以外的所有正文内容，根据需要添加chapX.tex)。
    > + chap1.tex: 第一章。
    > + chap2.tex: 第二章。
    > + conclusion.tex: 结论。
    > + papers.tex: 攻读学位期间发表的论文。
    > + acknowledgement.tex: 致谢。
4. images目录：图片存放目录。

参考文献格式说明
--------------------------------------------------------
严格遵循中国国家标准《[GB/T 7714-2005: 文后参考文献著录规则](https://std.samr.gov.cn/gb/search/gbDetailed?id=71F772D78562D3A7E05397BE0A0AB82A)》。

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
