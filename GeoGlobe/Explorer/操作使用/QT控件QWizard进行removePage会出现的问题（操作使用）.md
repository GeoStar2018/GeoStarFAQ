# QT控件QWizard进行removePage会出现的问题 #


C++ QT控件中QWizard可以根据需要添加页（addPage）、删除页（removePage）
不过在进行删除页操作后，如果再进行添加页，需要将添加页前索引最后一页setFinalPage(false)
否则一定概率会出现QWizard还没有进入最后一页便出现完成按钮。