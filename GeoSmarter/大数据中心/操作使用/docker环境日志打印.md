问题描述：

帮助项目组排查问题，打印tomcat实时日志


问题解答：

docker ps

docker exec -it a739 /bin/bash

docker logs -f a739d4ca17f0

docker logs -f -t --tail 100 a7