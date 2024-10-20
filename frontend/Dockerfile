FROM nginx
COPY code /usr/share/nginx/html
RUN rm -rf /etc/nginx/nginx.conf
RUN rm -rf /etc/nginx/conf.d
COPY nginx.conf /etc/nginx/nginx.conf
COPY expense.conf /etc/nginx/default.d/expense.conf


# docker-volumes
# 1)un-named volumes
# 2)named volumes

# 24  20/10/24 02:48:06 cd expense-docker-using_bridge_network/
#    25  20/10/24 02:48:08 cd mysql/
#    26  20/10/24 02:51:28 cd
#    27  20/10/24 02:51:50 sudo mkdir nginx-html
#    28  20/10/24 02:51:55 ls -la
#    29  20/10/24 02:54:26 docker run -d -v /home/ec2-user/nginx-html:/usr/share/nginx/html -p 80:80 nginx
#    30  20/10/24 02:54:45 docker ps
#    31  20/10/24 03:45:43 ls -la
#    32  20/10/24 03:46:16 docker run -d -v /home/ec2-user/nginx-html:/usr/share/nginx/html -p 80:80 nginx
#    33  20/10/24 03:46:27 docker ps
#    34  20/10/24 03:46:46 docker exec -it a7
#    35  20/10/24 03:46:53 docker exec -it a75df2ef7387
#    36  20/10/24 03:46:57 docker exec -it a7 bash
#    37  20/10/24 03:47:42 cd nginx-html/
#    38  20/10/24 03:47:43 ls -la
#    39  20/10/24 03:49:35 docker rm -rf nginx-html
#    40  20/10/24 03:49:37 cd ../
#    41  20/10/24 03:49:40 docker rm -rf nginx-html
#    42  20/10/24 03:49:49 sudo rm -rf nginx-html
#    43  20/10/24 03:49:53 ls -la
#    44  20/10/24 03:50:00 docker ps
#    45  20/10/24 03:50:05 docker rm -f a7
#    46  20/10/24 03:50:08 docker ps
#    47  20/10/24 03:50:11 docker images
#    48  20/10/24 03:50:22 docker rm 3b
#    49  20/10/24 03:50:34 docker rmi 3b
#    50  20/10/24 03:50:40 docker images
#    51  20/10/24 03:50:52 docker network ls
#    52  20/10/24 03:51:01 docker volume ls
#    53  20/10/24 03:51:06 docker volumes ls
#    54  20/10/24 03:51:14 docker volume create mysql
#    55  20/10/24 03:51:18 docker volume ls
#    56  20/10/24 03:54:22 docker inspect mysql
#    57  20/10/24 03:54:54 docker run -d -v mysql:/usr/share/nginx/html -p 80:80 nginx
#    58  20/10/24 03:55:02 docker ps
#    59  20/10/24 03:55:13 docker exec -it 03b76e4617ad
#    60  20/10/24 03:55:17 docker exec -it 03b76e4617ad bash
#    61  20/10/24 03:57:23 docker rm -f 03b76e4617ad
#    62  20/10/24 03:57:25 docker ps
#    63  20/10/24 03:58:15 docker run -d -v mysql:/usr/share/nginx/html -p 80:80 nginx
#    64  20/10/24 03:58:20 docker ps
#    65  20/10/24 03:58:29 docker exec -it 136cedcf9760 bash
#    66  20/10/24 03:58:59 cd m
#    67  20/10/24 03:59:04 cd mysql
#    68  20/10/24 03:59:06 ls -la
#    69  20/10/24 03:59:15 docker volume ls
#    70  20/10/24 04:00:07 cd /var/lib
#    71  20/10/24 04:00:09 ls -la
#    72  20/10/24 03:45:43 ls -la
#    73  20/10/24 03:46:16 docker run -d -v /home/ec2-user/nginx-html:/usr/share/nginx/html -p 80:80 nginx
#    74  20/10/24 03:46:27 docker ps
#    75  20/10/24 03:46:46 docker exec -it a7
#    76  20/10/24 03:46:53 docker exec -it a75df2ef7387
#    77  20/10/24 03:46:57 docker exec -it a7 bash
#    78  20/10/24 03:47:42 cd nginx-html/
#    79  20/10/24 03:47:43 ls -la
#    80  20/10/24 03:49:35 docker rm -rf nginx-html
#    81  20/10/24 03:49:37 cd ../
#    82  20/10/24 03:49:40 docker rm -rf nginx-html
#    83  20/10/24 03:49:49 sudo rm -rf nginx-html
#    84  20/10/24 03:49:53 ls -la
#    85  20/10/24 03:50:00 docker ps
#    86  20/10/24 03:50:05 docker rm -f a7
#    87  20/10/24 03:50:08 docker ps
#    88  20/10/24 03:50:11 docker images
#    89  20/10/24 03:50:22 docker rm 3b
#    90  20/10/24 03:50:34 docker rmi 3b
#    91  20/10/24 03:50:40 docker images
#    92  20/10/24 03:50:52 docker network ls
#    93  20/10/24 03:51:01 docker volume ls
#    94  20/10/24 03:51:06 docker volumes ls
#    95  20/10/24 03:51:14 docker volume create mysql
#    96  20/10/24 03:51:18 docker volume ls
#    97  20/10/24 03:54:22 docker inspect mysql
#    98  20/10/24 03:54:54 docker run -d -v mysql:/usr/share/nginx/html -p 80:80 nginx
#    99  20/10/24 03:55:02 docker ps
#   100  20/10/24 03:55:13 docker exec -it 03b76e4617ad
#   101  20/10/24 03:55:17 docker exec -it 03b76e4617ad bash
#   102  20/10/24 03:57:23 docker rm -f 03b76e4617ad
#   103  20/10/24 03:57:25 docker ps
#   104  20/10/24 03:58:15 docker run -d -v mysql:/usr/share/nginx/html -p 80:80 nginx
#   105  20/10/24 03:58:20 docker ps
#   106  20/10/24 03:58:29 docker exec -it 136cedcf9760 bash
#   107  20/10/24 03:58:59 cd m
#   108  20/10/24 03:59:04 cd mysql
#   109  20/10/24 03:59:06 ls -la
#   110  20/10/24 03:59:15 docker volume ls
#   111  20/10/24 04:00:07 cd /var/lib
#   112  20/10/24 04:00:09 ls -la
#   113  20/10/24 04:47:52 docker ps
#   114  20/10/24 04:47:58 docker volume ls
#   115  20/10/24 04:52:29 docker inspect -it mysql
#   116  20/10/24 04:52:34 docker inspect mysql
#   117  20/10/24 04:52:40 docker exec -it mysql bash
#   118  20/10/24 04:53:11 docker exec -it mysql /bin/bash
#   119  20/10/24 04:53:26 docker ps
#   120  20/10/24 04:53:40 docker exec -it 136cedcf9760 /bin/bash
#   121  20/10/24 04:55:42 docker volume inspect mysql
#   122  20/10/24 04:56:01 cd /var/lib/docker
#   123  20/10/24 04:56:12 sudo cd /var/lib/docker/volumes
#   124  20/10/24 04:56:14 ls -la
#   125  20/10/24 04:56:23 sudo cd /var/lib