问题描述：

2019年10版基线docker版大数据中心dup工具，计算节点添加失败




问题解答：


缺少一条与spark相关的网关，需要手动执行命令添加（docker network create -d overlay --attachable spark）

