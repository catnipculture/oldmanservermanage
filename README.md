> #### 作者主页：[舒克日记](https://blog.csdn.net/cativen)
>
>  简介：Java领域优质创作者、Java项目、学习资料、技术互助
>
> <b><font color=red>文中获取源码</font></b>

# 项目介绍

社区养老服务系统有管理员，用户两个角色。

管理员功能有个人中心，用户管理，服务种类管理，社区服务管理，服务预约管理，物品种类管理，物品信息管理，借用信息管理，归还信息管理，活动分离管理，社区活动管理，活动报名管理，疫情监控管理，物业收费管理，资讯中心管理，意见中心管理，系统管理。

用户可以注册登录，查看管理员发布的各中心信息，可以服务预约，借用归还，活动报名，发布自己的疫情监控信息，查看物业收费等操作。

社区养老服务系统的开发根据操作人员需要设计的界面简洁美观，在功能模块布局上跟同类型网站保持一致，程序在实现基本要求功能时，也为数据信息面临的安全问题提供了一些实用的解决方案。

# 环境要求

1.运行环境：最好是java jdk1.8,我们在这个平台上运行的。其他版本理论上也可以。

2.IDE环境：IDEA,Eclipse,Myeclipse都可以。推荐IDEA;

3.tomcat环境：Tomcat7.x,8.X,9.x版本均可

4.硬件环境：windows7/8/10 4G内存以上；或者Mac OS;

5.是否Maven项目：是；查看源码目录中是否包含pom.xml;若包含，则为maven项目，否则为非maven.项目

6.数据库：MySql5.7/8.0等版本均可；

# 技术栈

运行环境：jdk8 + tomcat9 + mysql5.7 + windows10

服务端技术：SpringBoot + MyBatis + Vue + Bootstrap + jQuery

# 使用说明

1.使用Navicati或者其它工具，在mysql中创建对应sq文件名称的数据库，并导入项目的sql文件；

2.使用IDEA/Eclipse/MyEclipse导入项目，修改配置，运行项目；

3.将项目中config-propertiesi配置文件中的数据库配置改为自己的配置，然后运行；

# 运行指导

idea导入源码空间站顶目教程说明(Vindows版)-ssm篇：

http://mtw.so/5MHvZq

源码地址：[http://www.codegym.top](http://www.codegym.top/)



# 运行截图

## 文档截图

![img](https://img-blog.csdnimg.cn/img_convert/44468afb1803e3f045511ae7e630f242.png)

![springboot253社区养老服务系统0](https://img-blog.csdnimg.cn/img_convert/c265052a5c22f3ba811bc007862c8ca2.png)

![springboot253社区养老服务系统1](https://img-blog.csdnimg.cn/img_convert/02dd0e927a082553640b6551ea9d4287.png)

![springboot253社区养老服务系统2](https://img-blog.csdnimg.cn/img_convert/3635aa8708c1368de1d9800c0b396f2c.png)

![springboot253社区养老服务系统3](https://img-blog.csdnimg.cn/img_convert/e4bc66165cc75ab7dcac236be30cec84.png)

![springboot253社区养老服务系统4](https://img-blog.csdnimg.cn/img_convert/92a8294ee4ff880d04418ebf92526d44.png)

![springboot253社区养老服务系统5](https://img-blog.csdnimg.cn/img_convert/91d107024a77985972e50eb1fbd4eea7.png)

![springboot253社区养老服务系统6](https://img-blog.csdnimg.cn/img_convert/1ff1832fa72f1d07576aa806dfe1e375.png)

![springboot253社区养老服务系统7](https://img-blog.csdnimg.cn/img_convert/3c75d96c3d576298e7bad83d2dbb7a8f.png)

![springboot253社区养老服务系统8](https://img-blog.csdnimg.cn/img_convert/d8d08ccfc540826b19f3244c3d3660e2.png)

### 代码

```
    // 获取系统内存信息
        long systemTotalMemory = osBean.getTotalPhysicalMemorySize();
        long systemFreeMemory = osBean.getFreePhysicalMemorySize();
        long systemUsedMemory = systemTotalMemory - systemFreeMemory;
        double systemMemoryUsage = (double) systemUsedMemory / systemTotalMemory * 100;
        BigDecimal systemMemoryPercent = new BigDecimal(systemMemoryUsage);
        systemMemoryPercent = systemMemoryPercent.setScale(1, RoundingMode.HALF_UP); // 设置小数点后一位，并四舍五
        BigDecimal systemTotalMemoryBigDecimal = convertLongToBigDecimal(systemTotalMemory);
        BigDecimal systemUsedMemoryBigDecimal = convertLongToBigDecimal(systemUsedMemory);
        log.info("系统总内存: {}G", systemTotalMemoryBigDecimal);
        log.info("系统已用内存: {}G，内存占用:{}%", systemUsedMemoryBigDecimal, systemMemoryPercent);
        dto.setSystemTotalMemory(systemTotalMemoryBigDecimal);
        dto.setSystemUsedMemory(systemUsedMemoryBigDecimal);
        dto.setSystemMemoryUsage(systemMemoryPercent);
```
