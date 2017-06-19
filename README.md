# atm
part 2-2 ATM program

1. ATM系统，分用户和管理员两个入口
    (1). atm.py -> 用户功能： 账户信息、还款、取款、转账、账单
    (2). manage.py -> 管理员功能：查询账户、添加账户、修改密码、修改额度、锁住和解锁账户

2. shopping.py -> 购物商城功能： 商品列表、加入购物车、银行账户验证结账、购买记录

功能全部用python标准库实现，用到os, time, re, json, 函数, 模块, 类的知识。

程序结构：
Atm/
    - __init__.py
    - README                        #文档
    - atm/                          #atm主程序目录
        - __init__.py
        - bin/                      #执行文件目录
            - __init__.py
            - atm.py                #用户端
            - manage.py             #管理端
        - conf/
            - __init__.py
        - core/                     #主程序目录
            - __init__.py
            - accounts.py           #账户管理的接口
            - auth.py               #账户验证模块
            - logger.py             #日志模块
            - main.py               #主程序逻辑处理模块
            - transaction.py        #交易中心模块
        - db/
            - __init__.py
            - accounts/             #每个账户各有一个数据文件，以账户名命名的json文件
                - __init__.py
                - admin.json        #管理员账户数据，开始设置密码自动创建
        - logs/
            - __init__.py
            - transaction.log       #交易中心日志
    - shopping_mall                 #购物商城程序目录
        - __init__.py
        - bin/
            - __init__.py
            - shopping.py           #购物商城
        - core/
            - __init__.py
            - main.py               #主程序
        - conf/
            - __init__.py
            - goods.json            #商品列表
        - logs/
            - __init__.py
            - history.log           #购买记录
    - flow.png                      #流程图
