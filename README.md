# 原创地址
	https://github.com/Curzibn/Luban
	
# 功能（压缩+放大缩小）

        Luban.with(this)
                .load(file)
                .putZoom(0.7f)
                .setCompressListener(new OnCompressListener() {
                    @Override
                    public void onStart() {
                        Toast.makeText(MainActivity.this, "I'm start", Toast.LENGTH_SHORT).show();
                    }

                    @Override
                    public void onSuccess(File file) {
                        Log.i("path", file.getAbsolutePath());

                        Glide.with(MainActivity.this).load(file).into(image);

                        thumbFileSize.setText(file.length() / 1024 + "k");
                        thumbImageSize.setText(computeSize(file)[0] + "*" + computeSize(file)[1]);
                    }

                    @Override
                    public void onError(Throwable e) {

                    }
                }).launch();


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
	      compile 'com.github.banketree:LubanImage:1.0.0'
	}
