# Jypter Notebook

You can use Jupyter notebook from your browser by vising our server's
address http://10.30.5.4 to run python code for data analysis. If all
goes well, you shall be prompted for login upon visiting the link. If
your user account hasn't yet been created, you may request for account
creation with @wilkerje or someone else at the lab.

Few things to know about the Jypter notebook running in our system:
1. The instance running in our server is callled [the littlest jupyter
   hub](https://tljh.jupyter.org/en/latest/install/custom-server.html).
If you're trying to manage/configure the installation, the site
aforementioned has several helpful guides.
1. To learn more about the jupyter notebook, https://docs.jupyter.org/en/latest/.   

### Why
The rationale behind using a system like Jupyter notebook is to
provide a playground where there's data for the code to run on too.
Since most of what we do after data processing is data analysis, it
would be ideal if researchers have a platform where they can write
code without having to worry about the latest copy of data to run
their code on. In addition to data, a system like this also makes it
easy to share code for helper functions that all researchers might
find useful. 

### How can I install xxx package?
The administrator account is responsible for installing python
packages that are available in the playground. One admin account is
m23. If you're an adminstrator trying to manage python packages and
versions for your users and yourself, this article might be helpful
https://tljh.jupyter.org/en/latest/howto/env/user-environment.html.   

### How to get the data?
TODO

### How do I share my Jupyter notebook with another user/researcher easily?
TODO

### How to use m23 package modules?
Anything that's defined in m23 should be acessible through the jupyter
notebook. For example you could just go and do 

```
from m23.utils import rename

# now you could use the rename function as you wish
```

To make this possible, we have made the folder
`/home/m23/Desktop/python-helpers` readable by any user in the system.
This had to be done even though it might look like we're only using
one user in the system (which isn't technically true because at the
very least we are using `m23` as the root user and `jupyter-m23` user
for the jupyter notebook). And in the future, we might as well choose
to use the system using multiple user accounts to keep data of each
user separate.

The folder aforementioned has been inserted to the system path that
ipython in the jupyter looks for when starting the notebook. This has
been done through the code at `/home/jupyter-m23/.ipython/profile_default/00-first.py`.
Apparently, when upon starting a jupyter notebook, all the python code
in the folder `/home/jupyter-m23/.ipython/profile_default/` are
executed in lexographic order meaning `001.py` first, `002.py`
`003.py`. 
