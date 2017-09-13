```
        /*
            onclick 鼠标点击事件
            onchange 改变内容
            onfocus 得到焦点
            onblur 失去焦点
            1、xml extensible Markup Language 可扩展标记型语言 设计的宗旨是传输数据而不是显示数据
            xml标签没有预定义 需要用户自行定义标签
                标记型语言html 是标记型语言
                    也是使用标签来操作
                可扩展
                    html里面的标签是固定的 每个标签有特定的含义<h1><br/><hr/>
                    标签可以自己定义 可以写中文的标签<person></person><猫></猫>
                xml用途
                    html是用于显示数据 xml也可以显示数据(不是主要用途)
                    xml主要用于存储数据
                xml是w3c组织发布的技术
                有两个版本 1.0 1.1
                    使用都是1.0版本 (1.1版本不能向下兼容)
           2、xml的引用
                不同的系统之间传输数据
                    qq之间数据的传输
                        qq消息之间的传输格式
                            最早的时候使用字符串
                            string str="qq1:qq2:hello:1995-12-11";
                            可读性差 使用字符串不利于程序的维护
                            现在使用方式
                            string str ="
                            <message id ="1">
                            <sender>1000</sender>
                            <getter>2000</sender>
                            <content>hello</content>
                            <ip>11</ip>
                            </message>
                            "
                            利于程序的维护
                用来表示生活中有关系的数据
                    将图片转化为计算机能识别的 标签之类的
                经常用在配置文件
                    比如连接数据库 数据库的用户名和密码 数据名称
                    如果修改数据库的信息 不用修改源代码 修改配置文件即可
            3、xml的语法
                1、xml的文档声明
                    创建一个文件 后缀名是.xml
                    如果写xml 第一步必须要有一个文档声明 (写了文档声明后 表示写xml文件的内容)
                    <?xml version="1.0" encoding="gbk"?>
                    文档声明必须写在第一行第一列 不然出不来
                    属性
                        version xml的版本 1.0(使用) 1.1
                        encoding xml编码 gbk utf-8 iso8859-1(不包含中文)
                        standalone 属性说明文档是否需要依赖其他文件 yes/no
                    xml的中文乱码问题
                        保存的时候 用默认的gbk xml中的中文按照gbk查找
                        打开xml文件的时候打开使用设置的编码utf-8 到uft-8编码查找的与gbk不同
                        如果不想出现乱码就用相同的编码方式 用工具不会出现这种问题
                2、定义元素(标签)
                3、定义属性
                4、注释
                5、特殊字符
                6、CDATA区
                7、PI指令
            4、xml元素的定义
                标签定义
                标签定义有开始必须要有结束 <person></person>
                标签没有内容可以在标签内结束 比如<aa/>
                标签可以嵌套 但是必须要合理嵌套
                    合理嵌套 <aa><bb></bb></aa>
                    不合理嵌套 <aa><bb></aa></bb> 不正确
                一个xml中 只能有一个根标签 其他标签都是这个标签下面的标签
                在xml中会把空格和换行都当作内容来解析
                    下面的代码含义不同
                    <aa>ee</aa>
                    <aa>
                     ee
                    </aa>
                xml标签的命名规则
                    可以是中文
                    xml代码是区分大小写
                        <p></P> 这两个标签是不同的
                    不能以数字或 _(下划线) 开头
                        <2e><_ww>不正确
                    xml的标签不能以xml XML Xml等开头
                        <xmla><Xmla><XMLA>等不正确
                    xml的标签不能包含空格和冒号
                        <a b> <b:c> 都不正确
            5、xml中属性的定义
                html是标记型文档 可以有属性
                xml也是标记型文档 也可以有属性
                <person id1="ee"></person>
                属性定义的要求
                    一个标签上可以有多个属性
                   <person id1="ee" id2="2"></person>
                属性名称不能相同
                   <person id1="ee" id1="2"></person>  错误
                属性名称和属性值之间使用 = 属性值使用引号包起来 (可以是单引号 也可以是双引号)
                xml属性的名称规范和元素的名称规范一致
            6、xml中的注释
                写法 <!-- 注释 -->
                注意的地方
                    注释不能嵌套 有一部分会挂在外面
                        <!--<!-- -->-->
                 注释也不能放到第一行 第一行第一列必须放文档声明
            7、xml中的特殊字符
                如果想要在xml中显示 a<b 不能正常显示 因为把<当作标签
                如果想要显示 需要对特殊字符 <进行转义
                < &lt;
                > &gt;
                " &quot;
                ' &apos;
                & &amp;
            8、CDATA 区 可以解决 多个字符需要转译的操作
                把内容放在CDATA 区中就不需要进行转译
                写法
                    <![CDATA[内容]]>
            9、PI指令(处理指令)
                可以在xml中设置样式
                写法<?xml version="1.0" type="text/css" href="css的路径"?>
                设置样式 只能对英文标签名起作用 对于中文的标签名称不起作用
                xml的语法总结
                    所有的xml元素必须关闭标签
                    xml标签对大小写敏感
                    xml必须正确地嵌套顺序
                    xml必须有跟元素 只有一个
                    xml的属性须加引号
                    特殊字符必须转译 CDATA
                    xml中的空格 回车换行会在解析时被保留
            10、xml的约束
                为什么需要约束
                比如现在定义一个person的xml文件 只想要这个文件里面保存人的信息 比如name age
                写了一个标签<矛> 可以正常显示 符合语法规范 但是矛不是人的信息xml的标签是自定义的 需要技术来
                规定xml中出现的元素 这个时候需要约束
                xml的约束的技术 dtd的约束 和 schema约束
            11、dtd约束
                创建一个文件 后缀名 .dtd
                步骤
                    看xml中有多少个元素 有几个元素 dtd中写几个<!ELEMENT>
                    判断元素是简单元素还是复杂元素
                        简单元素 没有子元素
                            <!ELEMENT 元素名称(#PCDATA)>
                        复杂元素 有子元素的元素
                            <!ELEMENT 元素名称(子元素)>
                            <!ELEMENT person(name,age)>
                    在xml文件中引入dtd文件
                        <!DOCTYPE 根元素名称 SYSTEM "dtd文件的路径">
                打开xml文件使用浏览器打开 浏览器只负责校验xml的语法 不负责校验约束
                如果想要校验xml的约束 需要使用工具(myeclipse工具)
                    引入dtd 后只能出现name和age 如果多写了一个a会提示出错
            12、dtd的三种引入方式
                1、引入外部的dtd文件
                    <!DOCTYPE 跟元素名称 SYSTEM "dtd路径">
                2、使用内部的dtd文件
                    <!DOCTYPE 根元素名称[
                        <!ELEMENT person (name,age)>
                        <!ELEMENT name (#PCDATA)>
                        <!ELEMENT age (#PCDATA)>
                    ]>
                3、使用外部的dtd文件(网络上的dtd文件)
                    <!DOCTYPE 跟元素 PUBLIC "DTD名称" "DTD文档的URL">
                    后面的struts2 使用配置文件 使用外部的dtd文件
                    <!DOCTYPE struts PUBLIC "-//Apache Software Foundation//DTD Struts Configuration 2.0//EN"
                    "http://struts.apahe.org/dtds/struts-2.0.dtd">
            13、使用dtd来定义元素
                语法 <!ELEMENT 元素名 约束>
                简单元素 (#PCDATA) 约束name是字符串内省
                        EMPTY   元素为空 没有内容
                             <a></a>
                        ANY     任意
                复杂元素 <!ELEMENT person(name,age) >
                            子元素只能出现一次
                        <!ELEMENT 元素名称(子元素)>
                        表示子元素出现的次数
                            + 一次或多次
                            ? 表示出现0次或1次
                            * 表示零次或多次
                       子元素直接使用逗号进行隔开
                            表示元素出现的顺序
                       子元素直接用|隔开
                            只能出现范围中的任意一个 (枚举)
            14、使用dtd定义属性
                语法 <!ATTLIST 元素名称
                        属性名称 属性类型 属性的约束
                        >



```

```
<!DOCTYPE person [
    <!ELEMENT person (name,age,sex,birthday)>
    <!ELEMENT name (#PCDATA)>
    <!ELEMENT age (#PCDATA)>
    <!ELEMENT sex EMPTY>
    <!ELEMENT birthday (#PCDATA)>
    <!ATTLIST birthday
            ID1 CDATA #REQUIRED>
    ]>




<person>
    <name>张三</name>
    <age>11</age>
    <sex></sex>
    <birthday ID1="11" ></birthday> ID1 这个属性必须出现
</person>

```
