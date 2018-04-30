# ansible note

## python虚拟环境

- 安装python虚拟环境

> pip install virtualenv

> pip install virtualenvwrapper

> pip install autoenv

- 需要将两行放在.bashrc/.zshrc(mac)

> export WORKON_HOME="$HOME/virtualenvs"

> source  .bashrc

> source /usr/local/bin/virtualenvwrapper.sh

- 指定创建python虚拟环境的python版本
> mkvirtualenv py27 --python=python2.7
> mkvirtualenv py36  --python=/usr/local/Cellar/python3/3.6.1/bin/python3


## ansible install
-  pip install ansible


## ansible configure


> export ANSIBLE_CONFIG=/virtualenvs/py2/ansible/ansible.cfg


## playbook优势

- 便于控制好依赖
- 可以复用
- 使用yaml语法


## playbook语法
### playbook基础使用

> ansible-playbook play.yml [options]
  

### yaml语法和变量
    ---   //表示开始
  
    -     //表示列表
  
    :     //:后面需要空1格
  
    大小写敏感

- 支持数据类型
  > 字典/列表/纯


- {{variable_name}}  变量的引用




### 循环条件

    with_items:标准循环
    with_nested:嵌套循环
    with_dict:遍历字典
    with_together:并行遍历列表
    with_indexed_items:遍历列表和索引
    with_file:遍历文件和索引
    with_fileglod:遍历目录文件
    until:重试循环
    with_firsh_found:查找第一个匹配文件
    with_random_choice:随机选择
    with_sequence:在序列中循环
    
### ansible核心类位置
    from ansible.parsing.dataloader import DataLoader
    from ansible.vars.manager import VariableManager
    from ansible.inventory.manager import InventoryManager
    from ansible.playbook.play import Play
    from ansible.executor.task_queue_manager import TaskQueueManager
    from ansible.plugins.callback import CallbackBase
    from ansible.executor.playbook_executor import PlaybookExecutor
    from ansible.inventory.host import  Host,Group

### ansible核心类介绍
    DataLoader:用于读取yaml,json格式文件
    Play:存储执行hosts的角色信息
    TaskQueueManager:ansible底层用到的任务队列
    PlaybookExecutor:核心类执行playbook
    CallbackBase:状态回调，各种成功失败状态
    InventoryManager:用于导入inventory文件
    VariableManager:用于存储各类变量信息
    Host,Group:操作单个主机或主机组信息
    
    
    InventoryManager调用 --->  VariableManager调用
                          |
          ad-hoc模式调用       playbook模式调用
    callback改写
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    








