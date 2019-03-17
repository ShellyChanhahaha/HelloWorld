# 实验内容

此为一个验证activity生命周期的实验，用log检验activity生命周期中onCreate()、onStart()、onResume()、onPause()、onStop()、onDestroy()的函数实现，从而探索其生命周期的步骤。

# 主要代码

这里主要是MainActivity.java的代码。

```java
package com.hfad.helloworld;

import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.util.Log;

public class MainActivity extends AppCompatActivity {

​    private static final String TAG = "ActivityLifecycle";

​    @Override
​    protected void onCreate(Bundle savedInstanceState) {
​        super.onCreate(savedInstanceState);
​        setContentView(R.layout.activity_main);
​        Log.d(TAG, "onCreate");
​    }

​    @Override
​    protected void onStart() {
​        super.onStart();
​        Log.d(TAG, "onStart");
​    }

​    @Override
​    protected void onResume() {
​        super.onResume();
​        Log.d(TAG, "onResume");

​    }

​    @Override
​    protected void onStop() {
​        super.onStop();
​        Log.d(TAG, "onStop");

​    }

​    @Override
​    protected void onPause() {
​        super.onPause();
​        Log.d(TAG, "onPause");
​    }

​    @Override
​    protected void onDestroy() {
​        super.onDestroy();
​        Log.d(TAG, "onDestroy");
​    }
}
```



# 结果截图

## AndroidStudio上的结果截图

### onCreate

![oncreate](https://i.loli.net/2019/03/17/5c8da28abdc30.png)

### onStart

![onstart](https://i.loli.net/2019/03/17/5c8da642c59c6.png)

### onResume

![onresume](https://i.loli.net/2019/03/17/5c8da673db644.png)

### onPause

![onpause](https://i.loli.net/2019/03/17/5c8da6c35b6bf.png)

### onStop

![onstop1](https://i.loli.net/2019/03/17/5c8da717004f4.png)

### onDestroy

![ondestroy](https://i.loli.net/2019/03/17/5c8da74c98a36.png)

## 真机上的运行结果截图

![1552787587372](https://i.loli.net/2019/03/17/5c8da8944295d.png)