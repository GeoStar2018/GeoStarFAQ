# Doxygen自动生成文档工具常见配置 #

设置文档记录代码的所有记录   EXTRACT_ALL = YES   改为NO

屏蔽类的私有成员             EXTRACT_PRIVATE  = NO

屏蔽没有注释的成员           HIDE_UNDOC_MEMBERS     = YES

屏蔽没有注释的类             HIDE_UNDOC_CLASSES     = YES

防止出现乱码            INPUT_ENCODING         = GBK

显示头文件 SHOW_INCLUDE_FILES     = NO

目录树显示文件 SHOW_FILES     = YES

宏替换： MACRO_EXPANSION、EXPAND_ONLY_PREDEF选项都设置为YES后, EXPAND_AS_DEFINED选项中可以添加 a=b关系来替换头文件中定义的宏