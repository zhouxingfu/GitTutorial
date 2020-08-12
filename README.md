# GitTutorial


__commit message规范__　　

    <type>(<scope>): <subject>  
    <BLANK LINE>  
    <body>  
    <BLANK LINE>  
    <footer>  

## 1 type   　　

\#__主要type__  
_feat_:    增加新功能  
_fix_:     修复bug   

\#__特殊type__  
_docs_:    只改动了文档相关的内容　　
_style_:   不影响代码含义的改动，例如去掉空格、改变缩进、增删分号  
_build_:   构建工具的或者外部依赖的改动，例如webpack, npm  
_refactor_: 代码重构时使用　　
_revert_:   执行git revert打印的message  

\# 暂不使用type  
_test_:    增加测试或者修改现有测试　　
_perf_:    提高性能的改动　　
_ci_:      与CI有关的改动　　
_chore_:   不修改src或者test的其余修改，例如构建过程或辅助工具的变动　　

当一次改动包括主要type和特殊type时，统一采用　主要type.


## 2 scope  

scope也为必填项，用于描述改动的范围，格式为项目名/模块名，例如node-pc/common   rrd-h5/activity，而we-sdk不需指定模块名。如果一次commit修改多个模块，建议拆分成多次commit，以便更好追踪和维护。　　

## 3 body  

body　填写详细描述，主要描述　改动之前的情况和修改动机，对于小的修改不作要求，但是重大需求、更新等必须添加body来作说明。　　　

## 4 break changes　　
break changes　指明是否产生了破坏性修改，涉及break changes的改动必须指明该项，类似版本升级、接口参数减少、接口删除、迁移等。　　

## 5 affect issues  
affect issues指明是否影响了某个问题，例如我们使用jira时，我们在commit message中可以填写其影响的JIRA_ID，若要开启该功能需要先打通jira与gitlab[参考文档](https://docs.gitlab.com/ee/user/project/integrations/jira.html)  

有commitizen工具可以辅助我们编写规范的commit message.

[Git commit message 规范](https://zhuanlan.zhihu.com/p/69989048)