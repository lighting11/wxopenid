接口:
```
POST https://wechatec.brand.wljhealth.com/WX_WeixinWS/getOpenid.wx
```
请求参数:
参数名 | 必须 | 类型 | 说明
---|---|---|---
appid|是|string|公众号appid
code|是|string|授权码

响应:

```
{
    status: 业务结果 为1 代表获取成功  其它值代表获取失败
	content: {
    		openid: 用户openid
    		refresh_token: 用户刷新access_token
    		access_token: 网页授权接口调用凭证,注意：此access_token与基础支持的access_token不同
    		expires_in: access_token接口调用凭证超时时间，单位（秒）
    		scope: 用户授权的作用域，使用逗号（,）分隔
		}
	msg: status不为1时 会返回该字段 表示错误说明
}
```