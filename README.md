感谢：

ToClash 项目 Clash Bing 神机规则

功能：

支持直接通过ssR订阅生成clash配置文件

使用：

有三个.py文件

初级：建议使用SSR_CLash_NoGroup，没有节点分组，默认不配置DNS。不再更新

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
高级：建议使用SSR_Clash_HttpServer。此版解码方法优化，支持大多数机场。不需要修改代码，运行后托管地址输入http://127.0.0.1:8964/?+订阅地址

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
API：建议使用SSR_Clash_API。部署在VPS上，需要python3环境。同目录下放置general.yml 和lrules.yml 

API调用方式：

API功能1：
SSR订阅到Clash

调用：

假设你的订阅地址为：https://stc-dns.com/link/Mzke     

最终地址为：http://ip:10086/https:!!stc-dns.com!link!Mzke

更新：

1.默认故障切换在前，如果你想让手动切换在前在最后加上@@yes

API功能2：
客制化纯SSR订阅，不是Clash订阅

调用：

假设你的订阅地址为https://stc-dns.com/link/Mzke    

假设你只想要香港和杭港节点，加上@香港@美国

最终地址为：

http://ip:10086/ssr/https:!!stc-dns.com!link!Mzke@香港@美国

说明：如果报错，说明你的客户端不支持中文URL，先URL_Encode一下（Google）

更新：
1.假设你只想要香港1倍节点和杭港5倍节点，为@香港&1倍@杭港&5倍

API功能3：
客制化SSR_Clash订阅

调用：

假设你的订阅地址为https://stc-dns.com/link/Mzke    

假设你只想要香港和杭港节点，加上@香港@美国

最终地址为：

http://ip:10086/https:!!stc-dns.com!link!Mzke@香港@美国
说明：如果报错，说明你的客户端不支持中文URL，先URL_Encode一下（Google）

更新：
1.假设你只想要香港1倍节点和杭港5倍节点，为@香港&1倍@杭港&5倍
2.默认故障切换在前，如果你想让手动切换在前在最后加上@@yes



问题：

报错大概率是网络原因
本地到Github会概率无法下载规则
不适用于所有机场，STC,TIMO经过测试。
