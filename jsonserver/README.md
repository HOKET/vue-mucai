//get方式
//获取所有用户信息
http://localhost:3000/users
//获取id为1的用户信息
http://localhost:3000/users/1
//获取公司的所有信息
http://localhost:3000/companies
//获取单个公司的信息
http://localhost:3000/companies/1
//获取所有公司id为3的用户
http://localhost:3000/companies/3/users
//根据公司名字获取信息
http://localhost:3000/companies?name=Google
//根据多个名字获取公司信息
http://localhost:3000/companies?name=Google&name=Apple
//获取一页中只有两条数据
http://localhost:3000/companies?_page=1&_limit=2
//升序排序  desc降序  asc升序
http://localhost:3000/companies?_sort=name&_order=asc
//获取年龄为30以及30以上的
http://localhost:3000/users?age_gte=30
//获取年龄为30到40之间的
http://localhost:3000/users?age_gte=30&age_gte=40
//搜索用户信息
http://localhost:3000/users?q=d

<!-- 知识点总结如下： 
1、http://localhost:3000/db 访问的是db.json文件下的所有内容； 
2、http://localhost:3000/layoutList?categoryName= 模拟接口参数可筛选该目录下内容 
3、分页查询 参数为 _start, _end, _limit，并可添加其它参数筛选条件 
如：http://localhost:3000/posts?_start=6&_limit=3 
http://localhost:3000/posts?_start=3&_end=6 
4、排序 参数为_sort, _order 
如：http://localhost:3000/posts?_sort=id&_order=asc 
http://localhost:3000/posts?_sort=user,views&_order=desc,asc 
5、操作符 _gte, _lte, _ne, _like 
_gte大于，_lte小于， _ne非， _like模糊查询 
6、q全局搜索（模糊查询）  -->