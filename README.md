## git_submodule项目配置
1. 添加操作说明:
   1. `git submodule add http://gitlab.roboticplus.com:2022/web-front-end/web_bus web_bus`
   2. `git config -f .gitmodules submodule.web_bus.branch main` 指定分支
   3. `git config -f .gitmodules submodule.robim_data.branch devel` 指定分支
   4. 上述域名为gerrit固定地址，可根据自己账号地址修改
   5. 相关操作参考在线文档:`https://zhuanlan.zhihu.com/p/404615843`

2. 已有.gitmodules文件后拉取操作说明:
   1. `git submodule update --init --recursive`
   会根据.gitmodules中的配置对应拉取子仓文件
