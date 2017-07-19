# XAppDbg
一款调试用的工具



使用方法：
	1、在AS中导入包XAppDbgServer.jar
	2、在Eclipse打开XAServer
	3、从代码中的常量中删除final关键字，因此可以在运行时更改参数。 也可以将内部类的所有常量移动到一起
	4、添加代码
	//创建并启动调试服务器
	mServer = new XAppDbgServer（）;
	mServer.addModule（new XAppDbgPropertiesModule（Consts.class））;	
	mServer.start（）;
	第一行只是创建一个服务器实例。 XAppDbgPropertiesModule扫描对象或类的字段，并公开其找到的所有公共字段。 第三行启动服务器，它将在端口55011上监听。
	！！！！！为了使其工作，应用程序必须具有INTERNET权限 
	5、在手机上运行您正在开发的应用程序。
	6、在E:\Android\sdk\platform-tools中cmd执行adb forward tcp：55011 tcp：55011
	7、运行XAServer，点击connect localhost
	8、！！！！！！！！！改了数据后要按回车
	
