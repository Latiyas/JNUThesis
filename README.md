JNUThesis
==============================
[暨南大学硕博士学位论文Overleaf模板](https://github.com/Latiyas/JNUThesis)
==============================


缘起
--------------------------------------------------------
又是一年毕业季，辛辛苦苦写好的论文怎么保证格式的排版标准规范一直是令人头疼的问题。
在学术研究过程中，大家都开始接触并习惯于使用LaTeX进行论文的排版，那么是否也可以借助这个工具撰写毕业论文呢？暨南大学数据存储与集群计算实验室的Yongtao Zhou学长虽然已完成了博硕士学位论文LaTex模板，但因为时间久远，加之软件版本不断更替，使用较新的本地LaTeX编译生成PDF文件过程中出现了一些错误或警告没有解决。
同时，由于笔者论文写作经验较浅，一开始接触的便是Overleaf，所以情感上更倾向于在线版的Overleaf。私以为Overleaf存在以下几点优势：a.简洁，高效，省去了配置环境的麻烦；b.可以多人在线，共同编辑同一个文档。因此萌发了将暨南大学博硕士学位论文模板迁移至Overleaf上的念头。

本项目的主要工作是将Yongtao Zhou学长的暨南大学博硕士学位论文LaTeX模板迁移至Overleaf，同时根据同学们的反馈对格式继续进行完善。原始项目见[JNUMasterThesis](https://github.com/ytZhou/JNUMasterThesis)，再次感谢Yongtao Zhou学长前期的大量工作。参考文献借鉴了南京大学的Haixing Hu学长的项目，详情见[GBT7714-2005-BibTeX-Style](https://github.com/Haixing-Hu/GBT7714-2005-BibTeX-Style)。感谢Haixing Hu学长的工作。由于近几年又发布了新版的参考文献著录格式，自2024年起，本模板的参考文献标准将全部更新到《[GB/T 7714-2015: 信息与文献 参考文献著录规则](https://wjk.usst.edu.cn/2020/0523/c10336a220878/page.htm)》。精简版手册请查看知乎文章《[参考文献著录格式（国标GB/T 7714-2015）](https://zhuanlan.zhihu.com/p/355312827?ivk_sa=1024320u)》

本项目虽然侧重于在Overleaf上进行编译测试，但同样能够在本地Latex上的编译通过。部分同学也反映，本地编译的结果是正常的。由于作者精力有限，暂时没有余力对本地编译的所有问题进行一一排查，请有问题的同学自行百度解决。本项目在Overleaf网站上的共享链接为[https://cn.overleaf.com/read/pwvngpvxfxdd](https://cn.overleaf.com/read/pwvngpvxfxdd)，愿意使用Overleaf平台的同学可以直接拷贝本项目的Overleaf版或者上传Github项目到Overleaf上进行修改即可。

PS: 由于作者精力有限，对于同学们反映的一些小问题，一般会先在Overleaf项目中进行快速更新。除非有较大的变动，否则将会在一到两个月对Github上的项目进行一次全面更新，敬请谅解。


运行环境
--------------------------------------------------------
1. 在线注册Overleaf账号，依次点击"New Project->Upload Project->Upload Zipped Project"将文件上传至服务器。
2. 进入Project，找到"Menu"选项，将"Settings->Compiler"修改成"XeLaTeX"，将"Settings->Main document"设置为"main.tex"，选择"main.tex"进行编译即可。
3. 项目默认在texlive2022版本下运行。如果运行异常，建议检查"Settings->TeX Live version"的设置。


源码目录结构
--------------------------------------------------------
1. 根目录: JNUThesis.tex是主文件，".ttf"或".ttc"文件是需要用到的字体文件，"gbt7714-2015.bst"是参考文献格式文件。
2. bib目录：bib文件存放目录，默认文件是refs.bib。可将论文需要用到的参考文献拷贝到refs.bib中；或者使用你的文件，并修改JNUThesis.tex中的命令"\bibliography{bib/refs}"。
3. chapter目录(根据需要引用章节，引用方式为"\include{需要引用的章节名称}"):
    > + abstract.tex: 中英文摘要。
    > + acknowledgement.tex: 致谢。
    > + appendix.tex: 附录。
    > + chaps.tex: 正文章节引用(管理除了declaration, abstract, conclusion, paper以及acknowledgement以外的所有正文内容，根据需要添加chapX.tex)。
    > + chap1.tex: 第一章。
    > + chap2.tex: 第二章。
    > + conclusion.tex: 结论。
    > + declaration.tex：首页的论文信息，请自行填写个人及导师信息。
    > + libs.tex：根据需要引入宏包。
    > + papers.tex: 攻读学位期间发表的论文。
4. images目录：图片存放目录。


关于更新
--------------------------------------------------------
目前，本项目仍在持续更新中。根据一些同学的实际反馈，更多的细节正不断被完善，感谢所有给予鼓励和支持的同学和老师。

对于本项目的早期使用者，如果希望与本项目的版本保持同步，强烈建议您在提前备份好自己的项目文件后，重新下载本项目主目录下的文件（主要是JNUThesis.tex和gbt7714-2015.bst，它们分别控制着论文的排版格式与参考文献格式）去替换您项目中的对应文件。得益于内容与样式的分离，一般情况下，版本的更新都能成功。根据作者的经验，发生错误的大部分情况是，文件夹或者tex文件的名称不匹配；新增的函数引用或者自定义命令放在主文件中而不是libs.tex中，请使用者自行检查上述问题。

如遇到其他项目更新的问题或者发现了模板本身的漏洞，欢迎通过邮箱与作者联系。


论文撰写小技巧
--------------------------------------------------------
1. 首页的声明信息，可以在declaration.tex中进行填写。
2. 超过3个作者以上的中文参考文献，部分作者需要省略为”等“，可以在bib引用中额外增加参数”language={zh}“进行修复。
3. 默认使用\cite{}的引用会以上标形式出现。部分同学可能还会用到非上标的情况，比如“论文[1]展示了。。。”，因此在新版中可以使用\norcite{}进行非上标的引用。


已修复问题
--------------------------------------------------------
2024.06.25更新
1. 完善了模板中的一些小漏洞。（感谢Jiahong Liu和Qiyi Zhang同学的帮助）

2024.04.06更新
1. 将论文修改成双面模式，设置不同的奇偶页页眉，并可通过参数控制是否为打印输出。具体方法是，修改JNUThesis.tex中的命令\isprintfalse。\isprintfalse表示非打印模式，\isprinttrue表示为打印模式，会自动显示空白页以方便双面打印。（感谢Jianglong Cao和Yaoyao Hong同学的帮助）
2. 重新调整代码的顺序，方便查阅。

2024.03.26更新
1. 新增了附录页(如不需要，可在JNUThesis.tex中搜索关于“appendix”的命令注释或删除)，完善了引用的设置。（感谢Bifeng Guo同学的帮助）
2. 增加了图、表标题的一些新实例。（感谢Fangzhen Zhao、Fei Zhong、Xiaoquan Zhang几位同学的帮助）

2024.03.20更新
1. 将参考文献著录格式的标准更新到《GB/T 7714-2015》。（感谢Qiyi Zhang同学的帮助）
2. 增加了非上标的引用格式\norcite{}，修正了章节引用的一些问题。（感谢Jiahong Liu同学的帮助）

2024.02.19更新
1. 修正了目录显示的一些问题。（感谢Fei Zhong同学的帮助）

2024.01.23更新
1. 更新了部分代码示例。（感谢Jiahong Liu同学的帮助）

2024.01.12更新
1. 修正了声明中的字体大小。（感谢Nuosi Li同学的帮助）
2. 将声明页的内容与样式进行了分离。（感谢Zhenhao Gu同学的帮助）
3. 更新了算法环境。

2023.09.02更新
1. 完善了参考文献中的破折号问题，修正了一些页码错误。（感谢Bifeng Guo同学的帮助）

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


参考文献格式说明
--------------------------------------------------------
严格遵循中国国家标准《[GB/T 7714-2015: 信息与文献 参考文献著录规则](https://wjk.usst.edu.cn/2020/0523/c10336a220878/page.htm)》。


注意事项
--------------------------------------------------------
1. 由于Overleaf需要在线编译，编译速度较慢。因此，撰写文稿时可以仅引用当前编辑的章节方便快速查看。暂未使用的章节可以先行注释，当需要阅读全文时再全部引用。正文章节的引用一般是放在chaps.tex中。
2. JNUThesis.tex中已包含了许多项目的编译设置，建议将新增宏包的引用放在libs.tex中，方便对项目进行管理。
3. 免费的Overleaf账号所提供的最大编译时间是有限的，对于使用了大量的矢量图(SVD文件)或者内容较长(超过一百五十页)的论文，编译超时可能会导致无法生成PDF。根据作者的经验，将SVD图片等文件转换成JPEG、PNG或者PDF格式将有助于减少编译时间。另外，编译中的语法错误、语法警告也可能导致编译器在语法检查上花费更多时间。如果以上方法都解决不了问题，可以考虑本地编译，或者在Overleaf上体验免费会员/充值会员。最近，笔者发现国内也有一款在线LaTeX写作平台——[TexPage](https://texpage.com/)，价格可能更实惠点，仅供读者参考。


Author
--------------------------------------------------------
Ming Li

Email: li-ming96@foxmail.com
