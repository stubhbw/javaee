# JDBC

![1572232356791](.\assets\1572232356791.png)

## JDBC工作过程

1. 加载驱动，建立链接

   1.1 创建 Maven 项目，导入 JDBC 包（通过Maven坐标导入或者直接导入Jar包，下图是 Maven 坐标，Maven坐标可以通过IDE内嵌搜索或者网页搜索得到）

   ![1572156258111](.\assets\1572156258111.png)

   1.2 代码加载驱动

   ```
   Class.forName("驱动程序类名");//驱动程序类名，例如：oracle.jdbc.OracleDriver
   ```

   1.3 连接数据库

   ```
   Connection conn = DriverManager.getConnection(url,userName,password);
   ```

   ![1572157634218](.\assets\1572157634218.png)

2. 创建语句 Statement

   ```
   Statement stmt = conn.createStatement();
   ```

   ![1572158832290](.\assets\1572158832290.png)

   ![1572231776086](.\assets\1572231776086.png)

3. 执行SQL

   ![1572159330368](.\assets\1572159330368.png)

   这里创建表的语句，返回是 false ，因为创建语句没有结果集

4. 处理结果集

   ![1572159840974](.\assets\1572159840974.png)

5. 关闭连接

   ```
   conn.close();
   ```

## JDBC执行executeQuery()

![1572233188998](.\assets\1572233188998.png)

![1572235124319](.\assets\1572235124319.png)

## JDBC连接管理

