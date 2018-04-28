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
  

- yaml语法和变量 


