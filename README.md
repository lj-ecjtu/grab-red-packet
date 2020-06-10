# grab-red-packet
   
    基于Spring、 SpringMVC、 MyBatis框架，结吅Redis，模拟高并发抢红包场景。使用JavaScript模拟3万人同时抢红包，后台采用两种方案实现并进行性能对比。

    方案一：采用乐观锁并基于按次数重入机制实现高并发抢好包，保证高并发情况下的数据一致性；
    
    方案二：基于Redis、 Lua语言实现高并发抢红包，先将抢红包数据保存在Redis中，当红包库存为0时，新建一条线程将Redis中的抢红包数据分批次保存到MySQL数据库中。

    主要技术：Spring、 SpringMVC、 MyBatis、 Redis、 Lua、 JavaScript、 Tomcat、 MySQL
