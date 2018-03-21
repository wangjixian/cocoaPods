wangjixian's first blog.welcome!
在安装cocoapods时提示：
YAML safe loading is not available.Please upgrade psych to version that supports safe loading(>=2.0)
查看本机支持的镜像

[plain] view plain copy

1. gem sources -l  
如果没有(http://gems.ruby-china.org/)，没有的话，先删除其他的；

[plain] view plain copy

1. gem sources --remove 地址  
添加http://gems.ruby-china.org/

[plain] view plain copy

1. gem sources -a http://gems.ruby-china.org/  
然后执行

[plain] view plain copy

1. sudo gem install -n /usr/local/bin cocoapods --re  
没有问题的话，正常会看到下面的提示，说明安装成功

[plain] view plain copy

1. 21 gems installed  
初始化cocoapods

[plain] view plain copy

1. pod setup  

过程中多次出现如下错误
[!] /usr/bin/git clone https://github.com/CocoaPods/Specs.git master --progress

Cloning into 'master'...
remote: Counting objects: 2003128, done.        
remote: Compressing objects: 100% (362/362), done.        
error: RPC failed; curl 56 SSLRead() return error -9806 13.00 KiB/s    
fatal: The remote end hung up unexpectedly
fatal: early EOF
fatal: index-pack failed
￼
等等错误，解决方案就是没有解决。
一天setup了十几次，一天啥都没干就弄这个了！情况是这样的，每次setup进行一部分（最低百分之7，最高百分之60），就进行不下去了，过一分钟就开始报错，报的错误有时候一样、有时候不一样，我根据网上的评论，每出现一种问题就根据网上搜到的结论，进行尝试，但是后来发现不对，因为后来报的错，我刚才已经解决了，而且上一次报的不是这个错，上一次setup停止的地方比这还靠前，反正就是感觉报的错误就这几个，并且随机出现。我就怀疑根本没有问题，就是网络的原因，就在下班的时候，重新setup了一遍，这一次很顺利。
所以，遇到该问题的小伙伴建议换个好点的网络环境再操作。
