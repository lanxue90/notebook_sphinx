sphinx
======

install ::

   pip3 install sphinx sphinx_rtd_theme

config

a, vim conf.py   修改主题 ::

   html_theme = 'sphinx_rtd_theme'
   
b, vim Makefile  修改Makefile，make后直接上传github ::

   github:
        @make html && cp _build/html/* -r ../lanxue90.github.io && cd ../lanxue90.github.io && git ad    d . && git commit -am"update" && git push 

c,vim index.rts 自动添加各目录下的index.rts文件 ::

   .. toctree::
   :maxdepth: 2
   :caption: Contents:
   :glob:
   */index

start::

    sphinx-quickstart -q -p notebook -a brook

make ::

   make html 生成html文件
   make      生成html文件，并上传github


github pages
   | 添加一个空文件到.nojekll到github仓库中 
   | ref:
   | https://pages.github.com
   | https://www.docslikecode.com/articles/github-pages-python-sphinx/

