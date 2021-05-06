#### Jenkins安装启动

- 下载安装

  - 提前安装jdk8

    sudo apt-get install openjdk-8-jdk

    java -version

  - 下载Generic Java package(.war) 

    https://www.jenkins.io/download/

  - Docker环境  docker pull jenkins/jenkins

  

- 启动方式

  - 方式一

    ```
    # war包启动方式
    java -jar jenkins.war
    java -jar jenkins.war --httpPort=9090 # 更换默认端口8080为9090
    ```

    1. 将[最新的稳定Jenkins WAR包](http://mirrors.jenkins.io/war-stable/latest/jenkins.war) 下载到您计算机上的相应目录。

    2. 在下载的目录内打开一个终端/命令提示符窗口到。

    3. 运行命令java -jar jenkins.war

    4. 浏览http://localhost:8080并等到*Unlock Jenkins*页面出现。

    5. 继续使用[Post-installation setup wizard](https://www.jenkins.io/zh/doc/book/installing/#setup-wizard)后面步骤设置向导。

       

- 官方说明

  https://www.jenkins.io/zh/doc/book/installing/