希云0.13.0版本，主要是增加了Lable支持，以及支持基于Lable的视图设置，当用户主机或容器数量较多时，可以做好区分。同时0.13.0版本恢复了本地镜像的管理功能。详细的Changelog如下：

## 0.13.0 新增加的功能：

- 新功能：容器和主机的标签管理0.13 版本增加了容器和主机的标签管理功能，你可以在创建容器时，为容器设置标签。或者为安装了 cSphere agent 的主机设置标签。

![add label](https://blog.csphere.cn/wp-content/uploads/2015/07/Screen-Shot-2015-07-31-at-7.01.13-PM-300x184.png)

- 新功能：容器和主机列表的视图设置，通过视图设置，可以让容器和主机列表只显示自己关注的条目。

![label view](https://blog.csphere.cn/wp-content/uploads/2015/07/Screen-Shot-2015-07-31-at-7.55.18-PM-300x160.png)

- 新功能：主机的下线维护你可以将当前运行有问题的主机，切换成维护状态。进入维护状态的主机上的容器和镜像，将不会在对应的列表中出现。当你把主机恢复时，数据将会重新出现。

![](https://blog.csphere.cn/wp-content/uploads/2015/07/Screen-Shot-2015-07-31-at-7.40.26-PM-300x18.png)

- 新功能：主机彻底删除你可以将不再需要通过 cSphere 管理的主机彻底删除。如果你希望把删除后的主机将重新连接到 cSphere, 请先将该主机的 csphere-agent 容器和数据目录（默认为 /data/csphere）删除，再重新安装 cSphere agent


## 0.13 还包含了以下重要改进

- 增加了面板事件通知的稳定性
- 对controller、agent及registry等重要容器进行危险操作时，系统会给出提示
- 增加了对容器崩溃的监控
- 私有 Docker Hub 增加 SSL 证书的设置，可以上传自己的 SSL 证书

## 如何升级

- 更新 Docker 到 1.6 或以上版本：希云从 0.13 起，将只对 Docker 1.6 及以上版本提供支持。如果你部署的 Docker 版本在 1.6 以下，请先升级 Docker.
- 根据安装说明重新安装 controller
- 更新完 controller 之后，在主机列表点击添加主机，根据图层提示的命令，在每台主机上执行该命令，完成 agent 的升级
 
## 关注希云
- 网站: https://csphere.cn
- 培训：https://csphere.cn/training
- 社区：https://discuss.csphere.cn
- 微信：cSphereCN

  ![qrcode](http://csphere.cn/s/02a64545-1f43-423d-9d15-72710f8d44f2.jpg)
