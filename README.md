# 原创地址
	https://github.com/Curzibn/Luban


导入第一步：

	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
	
导入第二步：添加引用

	dependencies {
		//综合包
	      compile 'com.github.banketree:Thinkcore:1.3.0'
	}