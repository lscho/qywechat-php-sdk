## 企业微信 SDK 修订版  

1.支持命名空间。
2.修复返回值差异问题。

> 企业微信的所有接口都会返回 errmsg 和 errcode ，所以在判断是否成功时不能以判断是否存在此字段为依据。原微信企业号 SKD 仅判断是否存在 errcode。

3.增加企业号的 CorpID 检测

> 企业号唯一标识为 CorpID，而原微信企业号 SKD 中是仍使用 appid 做为配置参数名，避免开发者误操作，现修订为检测到配置CorpID 而未配置 appid，则自动将 CorpID 设置为 appid 

4.增加 sendMessage 方法中 对 agentid 的默认设置，即如果存在 agentid 的配置项，则 sendMessage 所需数据即可省略
 agentid 。


