# 关于容器的使用
## 了解整个项目流程架构
![Image text](https://tva1.sinaimg.cn/large/0081Kckwgy1gm0yngkx57j30u00vu4qp.jpg)
## 数据存储的结构，也相当于实体类，所需的成员变量
![Image text](https://tva1.sinaimg.cn/large/0081Kckwgy1gm0ypri9kuj31e00fwgnu.jpg)
## 技术要求
- JDK 版本为 1.8 或以上 
- 键盘输入 Scanner 类 
- 正则表达式 Pattern 类 
- 容器 ArrayList 类
- 排序方式(比较器排序)Comparator 接口，Collections 类的 sort 方法
## 对项目类的命名规范和实现逻辑
需要一个启动类启动项目，实体类类存储数据，输入校验的类，校验输入的信息（这里需要使用正则表达式来对输入的数据和允许的数据进行比较），以及菜单类展示菜单内容，实现每个菜单下的方法的实现。具体命名规范如下：
### 类名
App 对应 Application(程序入口类)
Menu 对应 Menu (菜单类)
Operate 对应 Operate (业务处理类)
Person 对应 Person (实体类)
TelNoteRegex 对应 TelNoteRegex(用户输入验证类) 
OrderByName 对应 OrderByName (姓名排序比较器) 
OrderByAge 对应 OrderByAge (年龄排序比较器) 
OrderBySex 对应 OrderBySex(性别排序比较器)
### 方法
#### App 类中方法
main() 启动程序方法 
start() 主菜单控制
#### Operate 类中方法
private List<Person> list 容器
addLogic() 用户添加记录业务逻辑控制 
searchLogic() 用户查询记录业务逻辑控制 
modifyLogic() 修改记录业务逻辑控制 
deleteLogic() 删除记录业务逻辑控制 
orderLogic() 排序记录业务逻辑控制 
addOperation () 添加新记录信息 
showAll() 查询全部记录
searchByName() 按姓名查询记录 
searchByAge() 按年龄查询记录 
searchBySex() 按性别查询记录 
searchByTelNum() 按电话号码查询记录 
searchByAdd() 按地址查询记录 
modifyOperation() 修改指定记录 
deleteOperation() 删除指定记录 
deleteAllOperation() 删除全部记录 
orderName() 按用户姓名排序记录 
orderAge() 按用户年龄排序记录 
orderSex() 按用户性别排序记录

#### TelNoteRegex 类中方法
menuItemValidate (int min, int max ) 对菜单输入选项的验证 nameValidate ( ) 对用户输入姓名的验证
ageValidate ( ) 对用户输入年龄的验证
sexValidate ( ) 对用户输入性别的验证
telNumValidate ( ) 对用户输入电话号码的验证 
addressValidate ( ) 对用户输入地址的验证
#### Menu 类中的方法 
#### mainMenu() 主菜单
addMenu () 添加记录菜单 
searchMenu () 查找记录菜单 
modifyMenu () 修改记录主菜单 
subModifyMenu () 修改记录子菜单 
deleteMenu () 删除记录菜单 
orderMenu () 排序记录菜单
#### Person 类中的方法
private int id; 用户序号属性
private String name; 用户姓名属性
private String age; 用户年龄属性
private String sex; 用户性别属性
private String telNum; 用户电话号码属性
private String address; 用户地址属性
Person() 无参数构造方法
Person(String name, String age, String sex, String telNum, String address) 有参数构造方法 
getName() 读取用户名
setName(String name) 设置用户名
getAge() 读取用户年龄
setAge(String age) 设置用户年龄
getSex() 读取用户性别
setSex(String sex) 设置用户性别
getTelNum() 读取用户电话号码
setTelNum (String telNum) 设置用户电话号码 getAddress() 读取用户地址
setAddress(String address) 设置用户地址 getID () 读取用户 ID 号
setID (int ID) 设置用户 ID 号
toString() 连接字符串方法
#### OrderByName 类中的方法名 
compare(Person p1, Person p2)根据姓名排序方法
#### OrderByAge 类中的方法名 
compare(Person p1, Person p2)根据年龄排序方法
#### OrderBySex 类中的方法名 
compare(Person p1, Person p2)根据性别排序方法

 



