# runstone2
这里有美团启动页面小人奔跑

#奔跑代码如下
private void initData() {

		mImageView.setBackgroundResource(R.anim.frame);
		// 通过ImageView对象拿到背景显示的AnimationDrawable
		mAnimation = (AnimationDrawable) mImageView.getBackground();// 获取图片背景
		// 为了防止在onCreate方法中只显示第一帧的解决方案之一
		mImageView.post(new Runnable() {
			@Override
			public void run() {
				mAnimation.start();
			}
		});
		mLoadingTv.setText("一大波小石头在向你奔来...");
	}
