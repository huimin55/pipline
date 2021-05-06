#### 什么是Jenkins的流水线

Jenkins流水线是一套插件，它支持实现和集成*continuous delivery（CD） pipelines* 到Jenkins。

对Jenkins 流水线的定义被写在一个文本文件中 (成为 [`Jenkinsfile`](https://www.jenkins.io/zh/doc/book/pipeline/jenkinsfile))，该文件可以被提交到项目的源代码的控制仓库。

### 流水线语法

`Jenkinsfile` 能使用两种语法进行编写 - 声明式和脚本化。

- 声明式流水线

  Jenkinsfile (Declarative Pipeline)

  ```groovy
  pipeline {
      agent any 1
      stages {
          stage('Build') { 2
              steps {
                  // 3
              }
          }
          stage('Test') { 4
              steps {
                  // 5
              }
          }
          stage('Deploy') { 6
              steps {
                  // 7
              }
          }
      }
  }
  ```

  1 在任何可用的代理上，执行流水线或它的任何阶段。
  2 定义 "Build" 阶段。
  3 执行与 "Build" 阶段相关的步骤。
  4 定义"Test" 阶段。
  5 执行与"Test" 阶段相关的步骤。
  6 定义 "Deploy" 阶段。
  7 执行与 "Deploy" 阶段相关的步骤。