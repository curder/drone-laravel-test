## Drone laravel Demo.

```
docker pull drone/drone
docker pull drone/agent
docker pull drillster/drone-volume-cache
docker pull lddsb/drone-dingtalk-message

docker pull mysql:5.7
docker pull node:10.16
docker pull lorisleiva/laravel-docker:latest
```

或通过下面的命令统一安装对应需要的镜像
```
# See: https://github.com/moby/moby/issues/16106#issuecomment-310781836
echo drone/agent drone/drone drillster/drone-volume-cache lddsb/drone-dingtalk-message mysql:5.7 node:10.16 lorisleiva/laravel-docker:latest | xargs -P10 -n1 docker pull
```


- 当提交到 stage 分支，将构建测试版本，即在测试站点可以访问变更
- 当提交到 master 分支，将构建测试版本和上线版本，即在测试站点和线上版本可以访问变更

[![Build Status](https://cloud.drone.io/api/badges/curder/drone-laravel-test/status.svg)](https://cloud.drone.io/curder/drone-laravel-test)

