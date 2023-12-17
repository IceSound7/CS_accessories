CS饰品商店

学号：202130442471

姓名：周逸熙

项目开发环境：

    操作系统：Windows7及更高的Windows版本
    Web服务器：Tomcat8.5.97
    数据库：MySQL8.0
    开发工具：IDEA2023.3.5
    浏览器：Edge

主要目录介绍：

-src

    -dao：存储与数据库进行交互的java类
    -filter：存储过滤器类以及一个判定管理员权限类
    -listener：存储一个Listener类监听和获取商品分类
    -model：存储java实体类，包括Goods、Order等
    -service：存储不同servlet用到的service方法的重载类，包括GoodsService、OrderService等
    -servlet：存储用到的Servlet类
    -utils：存储项目用到的工具类，包括DataSourceUtils和PriceUtils

-web

    -admin：存储网页后台管理系统的JSP页面文件和CSS、JS、图片等
    -WEB-INF：存放输出结果classes、依赖lib以及一个页面配置文件web.xml
    其余文件夹分别存放对应前后台系统用到的CSS、JS、字体样式和图片


项目部署：

1.配置c3p0连接池和本地SQL数据库连接：

    <property name="driverClass">com.mysql.cj.jdbc.Driver</property>
		<property name="jdbcUrl">jdbc:mysql://8.134.186.126:3306/cs_accessories?serverTimezone=UTC&amp;useUnicode=true&amp;characterEncoding=utf-8</property>
		<property name="user">CS_accessories</property>
		<property name="password">******</property>

2.配置模块依赖：将本地下载的Tomcat的lib添加到模块依赖项
