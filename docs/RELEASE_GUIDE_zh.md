# 更新包上传说明

本包于2026年10月12日整理，保持上次data、docs、metadata、README.md、CITATION.cff、SHA256SUMS.txt和.gitignore结构。21个Origin项目中BBR及各反应热力学参数项目改变，其余19个完全相同。具体单元格改动见metadata/cell_changes.csv，概览见docs/CHANGELOG.md。

1. 打开本文件夹，将内部内容上传到现有GitHub仓库根目录；不要把外层文件夹再套一层，也不要仅上传ZIP代替可浏览目录。
2. 网页一次最多100个文件；较方便的做法是分别上传data、docs、metadata及根目录文件，保持路径。Windows默认隐藏的.gitignore也包含在ZIP内。
3. 上传后核对BBR的40%组S/m为295.8，苯酚热力学汇总为-8.785，以及README版本说明。导出器没有为消除问题擅自改数值。
4. 原来的Zenodo版本DOI 10.5281/zenodo.23252663只对应旧档案。本ZIP应在同一Zenodo记录中以New version发布，不能把旧DOI当作新版文件DOI。
5. 新版本发布后，将新版本DOI写入CITATION.cff及论文数据声明/数据集参考文献。不要提前编造新DOI。
6. 本更新未新增许可。之前作者要求许可待团队确认，而旧Zenodo记录显示CC BY 4.0；发布时确认新版许可，并同步GitHub和Zenodo声明。
7. docs/KNOWN_ISSUES.md保留未解决的原始记录及复现边界。数值与稿件一致不等于热化学、主曲线或模型已经验证。

本包已重新生成SHA256SUMS.txt。以后改任何文件都应更新校验清单；校验清单本身不包含在其自身的哈希列表中。
