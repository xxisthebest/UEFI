# 安装Anaconda
- 进入指定目录进行安装
  ```
  sudo wget https://repo.anaconda.com/archive/Anaconda3-2024.10-1-Linux-x86_64.sh
  bash Anaconda3-2024.10-1-Linux-x86_64.sh
  ```
- 配置环境变量
  ```
  vi ~/.bashrc
  export PATH="/自己对应的路径名/anaconda3/bin:$PATH"
  :wq
  source ~/.bashrc
  ```
  此时在terminal中输入conda，会出现相关信息
- 
