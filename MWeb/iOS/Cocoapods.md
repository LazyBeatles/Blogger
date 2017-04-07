# Cocoapods

* Cocoapods失效的解决方法，地址如下：[http://www.jianshu.com/p/b64b4fd08d3c](http://www.jianshu.com/p/b64b4fd08d3c)
* pod失效的解决方法，`rvm default use ruby-2.3.1(将ruby换成高版本)`

	
rvm命令 | 作用
---- | ---------------------------
rvm list | 列出当前系统的ruby版本
rvm default use ruby-2.3.1 | 切换ruby到2.3.1版本

Cocoapods命令 | 作用
------------- | ----------------
pod repo remove master | 移除默认repo
pod repo add master https://gitcafe.com/akuandev/Specs.git | 添加新的master repo

```
使用Cocoapods的开发者，自然会体会过以下几个命令是如何的慢
pod install
pod update
pod repo update
有人提供了一个解决方案，如下：
pod install --verbose --no-repo-update
pod update --verbose --no-repo-update

实际上这两条命令是取消了repo的更新，从而变快了pod的速度。但是，假如开发者本地的repo真的已经过时了（就是第三方的地址list是旧的），则无法逃避repo的更新，还是要使用pod repo udpate
```

