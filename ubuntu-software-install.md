# ubuntu for sublime-test-3 install
```
	sudo add-apt-repository ppa:webupd8team/sublime-text-3

	sudo apt-get update 


	sudo apt-get install sublime-text-installer
```

# ubuntu for pycharm
	- https://www.jetbrains.com/pycharm/
	- Download Professional | Full-featured IDE for Python & Web development

# ubuntu for intelliJIDEA
	- https://www.jetbrains.com/idea/
	- Download Ultimate | For web and enterprise development 

# ubuntu for chromium web Browser
  keyboard `win` Key >> ubuntu software >> Enter >> search chromium web Browser >> selecting && install 

# ubuntu for env

```
whoami@whoami-ThinkCentre-E73:/opt/gitlab/books$ cat ~/.bashrc |tail -8
export JAVA_HOME=/opt/cloud/jdk
export IDEA_HOME=/opt/cloud/idea
export PY_HOME=/opt/cloud/pycharm

export PATH=.:$IDEA_HOME/bin:$PY_HOME/bin:$JAVA_HOME/bin:$PATH

export CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar

```

# ubuntu for dev


# ubuntu for git
```
sudo apt-get install git 	# install git

cd /opt/gitlab

git clone git@github.com:apache/ambari.git 	# git project

git branch -a    # all branch info list

git checkout -t origin/branch-2.2.2	# switch branch


whoami@whoami-ThinkCentre-E73:/opt/gitlab/ambari$ git branch
* branch-2.2.2
  trunk	  # default selecting

```

# ubuntu 16.4 for ambari
	https://cwiki.apache.org/confluence/display/AMBARI/Ambari+Development

- python 2.7

```
sudo sh setuptools-0.6c11-py2.7.egg
```

- install dependency node && npm
```
https://nodejs.org/dist/v0.10.44/	# version v0.10.44, 0.12.x won't work. 

whoami@whoami-ThinkCentre-E73:/opt/cloud/node/bin$ cat ~/.bashrc |grep NODE
export NODE_HOME=/opt/cloud/node
export PATH=.:$NODE_HOME/bin:$MVN_HOME/bin:$IDEA_HOME/bin:$PY_HOME/bin:$JAVA_HOME/bin:$PATH
```

# build ambari
	- https://cwiki.apache.org/confluence/display/AMBARI/Coding+Guidelines+for+Ambari
	
```
$ cd ambari/ambari-web/
$ sudo su - root
$ npm install -g brunch@1.7.20

$ exit


$ cd ambari/ambari-web
$ rm -rf node_modules public
$ npm install
$ ulimit -n 10000
$ brunch build

$ brunch watch --server (or use the shorthand: brunch w -s)

-- For example
whoami@whoami-ThinkCentre-E73:/opt/gitlab/ambari/ambari-web$ brunch w -s
15 Aug 11:17:58 - info: application started on http://localhost:3333/


$ mvn -B clean install package jdeb:jdeb -DskipTests -Dpython.ver="python >= 2.6" -Preplaceurl	#for ubuntu
```


# ubuntu for docker
```
 sudo apt-get install docker.io
 
 /etc/init.d/docker start

sudo systemctl stop docker.service
sudo systemctl start docker.service

sudo systemctl status docker.service

sudo docker images

```


spark-submit   --class streaming.core.StreamingApp \
--master yarn-cluster \
--name sql-interactive \
/tmp/streamingpro-0.3.4-SNAPSHOT-online-1.6.1.jar    \
-streaming.name sql-interactive    \
-streaming.platform spark   \
-streaming.rest true   \
-streaming.driver.port 9004   \
-streaming.spark.service true	\
-streaming.zk.servers bigdata-hdp-server-3:2181,bigdata-hdp-server-1:2181,bigdata-hdp-server-2:2181 \
-streaming.zk.conf_root_dir  /streamingpro/sparkstreaming 

+ '/zeppelin-' + zeppelin + '*.pid'

pid_file=glob.glob('/var/run/zeppelin-notebook' + '/zeppelin-'+ 'zeppelin'+ '*.pid')[0]
