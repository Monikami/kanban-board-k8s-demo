1. Without SQL connection backned IP will not come up

2021-07-26 20:34:04.005  INFO 1 --- [           main] o.apache.catalina.core.StandardService   : Starting service [Tomcat]
2021-07-26 20:34:04.006  INFO 1 --- [           main] org.apache.catalina.core.StandardEngine  : Starting Servlet engine: [Apache Tomcat/9.0.21]
2021-07-26 20:34:04.153  INFO 1 --- [           main] o.a.c.c.C.[Tomcat].[localhost].[/api]    : Initializing Spring embedded WebApplicationContext
2021-07-26 20:34:04.153  INFO 1 --- [           main] o.s.web.context.ContextLoader            : Root WebApplicationContext: initialization completed in 4093 ms
2021-07-26 20:34:04.985  INFO 1 --- [           main] com.zaxxer.hikari.HikariDataSource       : HikariPool-1 - Starting...
2021-07-26 20:34:06.067 ERROR 1 --- [           main] com.zaxxer.hikari.pool.HikariPool        : HikariPool-1 - Exception during pool initialization.

org.postgresql.util.PSQLException: The connection attempt failed.
        at org.postgresql.core.v3.ConnectionFactoryImpl.openConnectionImpl(ConnectionFactoryImpl.java:292) ~[postgresql-42.2.5.jar!/:42.2.5]
        at org.postgresql.core.ConnectionFactory.openConnection(ConnectionFactory.java:49) ~[postgresql-42.2.5.jar!/:42.2.5]
        at org.postgresql.jdbc.PgConnection.<init>(PgConnection.java:195) ~[postgresql-42.2.5.jar!/:42.2.5]
        at org.postgresql.Driver.makeConnection(Driver.java:454) ~[postgresql-42.2.5.jar!/:42.2.5]
        at org.postgresql.Driver.connect(Driver.java:256) ~[postgresql-42.2.5.jar!/:42.2.5]
        at com.zaxxer.hikari.util.DriverDataSource.getConnection(DriverDataSource.java:136) ~[HikariCP-3.2.0.jar!/:na]
        at com.zaxxer.hikari.pool.PoolBase.newConnection(PoolBase.java:369) ~[HikariCP-3.2.0.jar!/:na]
        at com.zaxxer.hikari.pool.PoolBase.newPoolEntry(PoolBase.java:198) ~[HikariCP-3.2.0.jar!/:na]
        at com.zaxxer.hikari.pool.HikariPool.createPoolEntry(HikariPool.java:467) [HikariCP-3.2.0.jar!/:na]
        at com.zaxxer.hikari.pool.HikariPool.checkFailFast(HikariPool.java:541) [HikariCP-3.2.0.jar!/:na]
        at com.zaxxer.hikari.pool.HikariPool.<init>(HikariPool.java:115) [HikariCP-3.2.0.jar!/:na]
        at com.zaxxer.hikari.HikariDataSource.getConnection(HikariDataSource.java:112) [HikariCP-3.2.0.jar!/:na]
        at liquibase.integration.spring.SpringLiquibase.afterPropertiesSet(SpringLiquibase.java:302) [liquibase-core-3.6.3.jar!/:na]
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.invokeInitMethods(AbstractAutowireCapableBeanFactory.java:1837) [spring-beans-5.1.8.RELEASE.jar!/:5.1.8.RELEASE]
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.initializeBean(AbstractAutowireCapableBeanFactory.java:1774) [spring-beans-5.1.8.RELEASE.jar!/:5.1.8.RELEASE]
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:593) [spring-beans-5.1.8.RELEASE.jar!/:5.1.8.RELEASE]
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:515) [spring-beans-5.1.8.RELEASE.jar!/:5.1.8.RELEASE]
        at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:320) [spring-beans-5.1.8.RELEASE.jar!/:5.1.8.RELEASE]
        at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:222) ~[spring-beans-5.1.8.RELEASE.jar!/


