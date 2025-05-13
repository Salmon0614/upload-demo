# upload-demo
分片上传和流式播放demo

# 技术栈
## 前端
Vue3 + Element Plus + Axios + Vue-router + Vuex

## 后端
Java17 + SpringBoot2.7.15 + Mybatis-Plus + MySQL8.0

# 数据库表

```sql
create table `file_info`
(
    id  int auto_increment
        primary key,
    url varchar(500) not null,
    constraint id
        unique (id),
    constraint url
        unique (url)
)
```
# 其他
配置文件自行修改，我这端口开在了 9090，上传文件存放地址为项目地址的 public/files

为了防止盗链盗资源等情况，我在播放请求接口逻辑里设置了指定请求有效referer

可以自行根据前端地址更改

有能力的也可以用 `Nginx` 技术进行防盗链