接口:
```
 POST https://wechatec.brand.wljhealth.com//WX_WeixinWS/registerWxJs.wx 
```
请求参数:
参数名 | 必须 | 类型 | 说明
---|---|---|---
outkey|是|string|公众号appid
url|是|string|注册jsapi的网页
响应:
```
{
status: 业务结果 为1 代表获取成功  其它值代表获取失败
content: {
    		appid: 公众号appid
    		url: 注册jspapi的网页
    		noncestr: 随机字符串
    		signature: 签名
    		timestamp: 时间戳
		}
msg: status不为1时 会返回该字段 表示错误说明
}
```