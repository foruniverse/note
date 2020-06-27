## mybatis



#### mybatis mapper.xml 写法



- 最简单的一个,查询表内所有数据

  比如说查询 用户表中所有用户

  ~~~ xml
  第一种 返回 LIST<User>
  如果使用select * 来查询的 那么实体类中的属性必须和数据表中对应的字段一模一样
  <select id ="selectAll" resultType="USer">
  	select * from user
  </select>
  
  第二种 返回 Map<String,Object>
  <select id ="selectALL_1" resultType = "map">
  	select name ,id ,sex from user
  </select>
  ~~~
  
- 插入时返回插入的行数,在mysql中有效

  ~~~xml
  <insert id="insertUser" useGeneratedKeys="true" keyProperty="userId" parameterType="cn.stu.entity.UserEntity">
      insert into user(userName,password,comment)  
      values(#{userName},#{password},#{comment})  
  </insert>
  通过 user.getId()获取插入的主键
  ~~~

  




~~~

~~~