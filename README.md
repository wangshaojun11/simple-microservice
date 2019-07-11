# simple-microservice
简单的微服务

## 部署须知 ##
  * 1.首先需要导入doc/db里面的数据库到自己的mysql
  * 2.修改部署的环境application.yml 里面的active配置为fat
  * 3.修改数据库配置，只需要修改application-fat.yml的数据库即可
  * 4.因为maven是子父模块的，直接再父模块统一打包即可
  * 5.启动portal之前请改动一下portal-service jar包里面的,resources->static->orderList.js和productList.js里面的三个异步请求网关的链接
      改为自己的网关外网地址即可。
  * 6.启动顺序：注册中心——网关——portal服务——商品服务——库存服务——订单服务
## 架构图 ##
![微服务架构图.jpg](https://i.loli.net/2019/06/21/5d0c9c1db1e2735393.jpg)
