## xUtils3简介

> 本项目只保留xutils3中的db模块

### 引入

Gradle
> compile 'im.unicolas:xutils3-db:3.5.1'

### 初始化
```java
// 在application的onCreate中初始化
@Override
public void onCreate() {
    super.onCreate();
    x.Ext.init(this);
    x.Ext.setDebug(BuildConfig.DEBUG); // 是否输出debug日志, 开启debug会影响性能.
    ...
}
```

### 使用数据库(更多示例参考sample项目)
```java
Parent test = db.selector(Parent.class).where("id", "in", new int[]{1, 3, 6}).findFirst();
long count = db.selector(Parent.class).where("name", "LIKE", "w%").and("age", ">", 32).count();
List<Parent> testList = db.selector(Parent.class).where("id", "between", new String[]{"1", "5"}).findAll();
```

----
### 关于作者
* Email： <wyouflf@qq.com>, <wyouflf@gmail.com>
* 有任何建议或者使用中遇到问题都可以给我发邮件, 你也可以加入QQ群：330445659(已满), 275967695, 257323060,
384426013, 176778777, 169852490, 261053948, 330108003, 技术交流，idea分享 *_*
---

### 我这边只是搬运工 ^_^

[这里是原地址](https://github.com/wyouflf/xUtils3)

---

###END