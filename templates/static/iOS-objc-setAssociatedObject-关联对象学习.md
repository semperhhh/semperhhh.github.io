
date: 2018-07-29 13:32:02
pid: 19012406;
tag: iOS;

---

# iOS-objc_setAssociatedObject 关联对象学习

## iOS-objc_setAssociatedObject 关联对象学习

> 关联对象就是runtime中的NSMutableDictionary

关联对象可以给某个object关联一个或多个其他对象,这些对象通过"键"来区分

关联对象相当于实例变量,在分类(catetory)里面不能创建实例变量,可以通过关联对象实现getter和setter,关联对象就可以解决这种问题.

有时需要在对象中存储一些额外的信息,而开发者无法创建出自己所写的子类实例来给对象的子类添加额外的属性.或者只是给某个类添加一个额外的属性,完全没必要继承出来一个子类.

~~~~objective-c
objc_setAssociatedObject 相当于 setValue:forKey 进行关联value对象

objc_getAssociatedObject 用来读取对象

objc_AssociationPolicy  属性 是设定该value在object内的属性，即 assgin, (retain,nonatomic)...等

 objc_removeAssociatedObjects 函数来移除一个关联对象，或者使用objc_setAssociatedObject函数将key指定的关联对象设置为nil。

key：要保证全局唯一，key与关联的对象是一一对应关系。必须全局唯一。通常用@selector(methodName)作为key。
value：要关联的对象。
policy：关联策略。有五种关联策略。
OBJC_ASSOCIATION_ASSIGN 等价于 @property(assign)。
OBJC_ASSOCIATION_RETAIN_NONATOMIC等价于 @property(strong, nonatomic)。
OBJC_ASSOCIATION_COPY_NONATOMIC等价于@property(copy, nonatomic)。
OBJC_ASSOCIATION_RETAIN等价于@property(strong,atomic)。
OBJC_ASSOCIATION_COPY等价于@property(copy, atomic)。
~~~~

### 关联对象的管理函数

~~~~objective-c
OBJC_EXPORT void objc_setAssociatedObject(id object, const void *key, id value, objc_AssociationPolicy policy)
    __OSX_AVAILABLE_STARTING(__MAC_10_6, __IPHONE_3_1);//存储
OBJC_EXPORT id objc_getAssociatedObject(id object, const void *key)
    __OSX_AVAILABLE_STARTING(__MAC_10_6, __IPHONE_3_1);//获取
    OBJC_EXPORT void objc_removeAssociatedObjects(id object)
    __OSX_AVAILABLE_STARTING(__MAC_10_6, __IPHONE_3_1);//移除某个对象身上的所有关联的对象.objc没有提供移除object神圣单个关联对象的函数.可以通过objc_setAssociatedObject传入nil来打到移除某个关联对象.
~~~~

#### 给category的property添加getter和setter

~~~~objective-c
catetory中声明一个属性
@property (nonatomic, copy) NSString *name;

//getter
-(NSString *)name {
	return objc_getAssociatedObject(self, key);
}

-(void)setName:(NSString *)name {
	// 第一个参数：给哪个对象添加关联
    // 第二个参数：关联的key，通过这个key获取
    // 第三个参数：关联的value
    // 第四个参数:关联的策略
    objc_setAssociatedObject(self, key, name, OBJC_ASSOCIATION_RETAIN_NONATOMIC);
}
~~~~
