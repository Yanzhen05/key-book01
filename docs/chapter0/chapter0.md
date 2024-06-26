# 第0章：序言

*Edit: Hao ZHAN*

---

## 1.关于《机器学习理论导引》

机器学习备受关注，机器学习的相关课程与教材可谓汗牛充栋。就国内教材而言，周志华的**《机器学习》**和李航的**《统计学习方法》**已然成为了广大学子入门机器学习的宝典。而 Mitchell 的 ***Machine Learning***， Duda 等人的 ***Pattern Classification***， Alpaydin 的 ***Introduction to Machine Learning***，则提供了一些古典风格的路径选择。若有更深入的需求， Bishop 的 ***Pattern Recognition and Machine Learning***， Murphy 的 ***Machine Learning - A Probabilistic Perspective***，Hastie 等人的 ***The Elements of Statistical Learning***，则可以系统性地给学习者提供帮助。以上的这些书籍还仅仅是广大学习材料中的一隅，似乎可以说无论国内精品，亦或海外译丛，都已不再缺乏。

然而，若是以**机器学习理论**的视角来考察国内的学习材料，则可以得出不同的结论。与上述描述机器学习算法（Machine Learning Algorithm）的著作不同，关注机器学习理论（Machine Learning Theory）书籍似乎并没有得到多少讨论。尽管在上述的这些著作中，或多或少都展开了对于理论的探讨，但篇幅极为有限——或为些许独立篇章，或为一点只言片语，难以满足广大学子理论学习、研究之渴求。

过去，机器学习理论的经典教材多以英文写作。上世纪末，围绕统计学习理论所展开的一系列讨论，产出了诸多经典文献。较为著名的有 Vapnik 的 ***The Nature of Statistical Learning Theory*** 和 ***Statistical Learning Theory***，以及 Devroye 等人的 ***A Probabilistic Theory of Pattern Recognition***。一些近期的讨论则是来自于 Shalev-Shwartz 和 Ben-David 的 ***Understanding Machine Learning***，以及 Mohri 等人的 ***Foundations of Machine Learning***。尽管 Vapnik 的两本著作，以及 ***Foundations of Machine Learning*** 都已有了优质的译作，但以中文来写作的、属于我们自己的机器学习理论入门著作的缺乏，仍旧是一个不大不小的遗憾。

而现在，周志华、王魏、高尉、张利军等老师所著的**《机器学习理论导引》**一书（下称《导引》），则填补这个空白。该书试图以通俗易懂的语言，为有志于学习机器学习理论和研究机器学习理论的读者提供一个入门的导引。该书主要涵盖七个部分，分别对应机器学习理论中的七个重要概念或理论工具，即：**可学性、（假设空间）复杂度、泛化界、稳定性、一致性、收敛率、遗憾界**。

学习机器学习理论虽不如学习机器学习算法那样，可以立即将所学付诸应用。但只要砥砺前行、深入学习，则不仅可领悟机器学习中的重要思想，亦可体会机器学习之奥妙。<sup>[1]</sup> 

--By: Hao ZHAN

## 2.关于《机器学习理论导引》NOTES

《导引》的NOTES，在团队内部又被戏称为《钥匙书》。《钥匙书》一名，取自《导引》一书的戏称——《宝箱书》，暗含抱关执钥，助诸位读者解惑之意。

《导引》是一本理论性较强的书籍，涉及大量的数学定理和各种证明。尽管撰写团队已尽可能降低了难度，但由于机器学习理论学习本身的特性，该书仍然对读者的数学背景提出了较高的要求。这难免会导致不求甚解的情形，影响学习效果；另一方面，由于篇幅所限，该书写作较为精炼，并非在各个章节都给出示例。读者每每遇到晦涩抽象之处，难免冥思苦索。

基于此两点，我们决定尝试编辑《钥匙书》这一参考笔记，来对《导引》一书作一些浅陋且皮毛的注脚。这既是着眼于那些阅读《导引》时遇到困难的读者，助其更快地走出迷雾；亦是对学习《导引》一书之过程的最好记录。

《钥匙书》的补充性工作，主要包括四个方面：

（1）**证明补充**：对部分证明的证明思路进行解释，对部分省略的证明过程进行补充。

（2）**案例补充**：增加解释案例，帮助读者理解。

（3）**概念补充**：介绍部分文中涉及、但未阐释的概念。

（4）**参考文献讲解**：对部分重要的参考文献进行介绍。

此外，由于《导引》一书的第一章节为基础知识补遗，简明易懂，因此《钥匙书》的内容从《导引》的第二章开始。

---
Update datetime: 2024/03/14

对于我个人感受而言，《机器学习理论导引》这是一本什么样的书呢，和《Understanding Machine Learning》 以及《Foundations of Machine Learning》一样，其实我称为“无用”之书，“无用”在于哪里呢，在于理论和实践效果的巨大Gap，经典的机器学习理论已经很难去解释深度学习包括现在生成式大模型如此令人惊讶的效果，但我依然相信未来将是站在现在肩膀上开出新的花朵，所以分析的结论不是最重要的，而是相关的思想和分析思路，而数学作为一种分析工具被使用，我依然期望，未来深度学习将会有更多的理论支撑，从而更好的指导实践相关工作，费曼说："What I cannot create, I do not understand." —— “凡我不能创造，我就不能理解”，期望大家能从相关理论中得到启迪，从而创造出更有意思的一些工作; 另一个方面而言，这是一本让人自省并且发现自己无知的书，不同于传统介绍机器学习算法的书籍，这本书需要大家有较好的数学理论功底，也将借助数学工具，从更为抽象的角度去分析机器学习算法的相关性质而非机器学习算法本身，这条路上未来的路还很漫长，《牧羊少年的奇幻漂流》中说"每个人的寻梦过程都是以'新手的运气'为开端，又总是以'对远征者的考验'收尾。"，期望大家能经历考验，终寻所梦。

由于《钥匙书》-v1.0 版本发布后一直受到相关学习小伙伴的关注，在过程中也有很多教材相关内容的疑问，由此，为更深入的对于相关知识进行理解，也为了记录团队进一步阅读机器学习理论相关书籍的记录，后续将持续对于《钥匙书》进行不定期更新，期望大家的关注。

--By: ML67

## 3.项目更新计划

项目组会优先完成「证明补充」、「案例补充」和「概念补充」的内容。「参考文献讲解」则在前三项工作完成后统一进行。更新计划如下：

​	2020/06/10：第2章、第3章

​	2020/07/10：第4章、第5章

​	2020/08/10：第6章、第7章

​	2020/09/10：第8章、总结

---
Update datetime: 2024/03/15

计划更新的内容：
1. 各个章节的注释补充扩展和说明
2. 章节相关引理的补充、证明和拓展分析
3. 章节内容补充、深入和扩展（添加相关 Understanding Machine Learning 和 Foundations of Machine Learning 的内容）
4. 其他章节之前内容的校订 
5. 统一全书markdown的格式

## 4.项目成员

[王茂霖](https://github.com/mlw67)：第2、3、4、5、6、7章内容的编辑，项目的二期更新修订		

[李一飞](https://github.com/leafy-lee)：第2、3、4、5、6、7章内容的编辑

[杨昱文](https://github.com/youngfish42)：部分内容的编辑

[Sm1les](https://github.com/Sm1les)：鼓励师

[张	雨](https://github.com/Drizzle-Zhang)：第2章部分内容的修改

[J.Hu](https://github.com/inlmouse)：第一章内容的编辑

[赵志民](https://github.com/zhimin-z)：项目第二阶段的更新与维护

[詹	好](https://github.com/zhanhao93)：项目规划与统筹负责；全书内容的编辑






---

[1] 关于学习理论的作用，可参阅《机器学习理论导引》1.5节内容。

