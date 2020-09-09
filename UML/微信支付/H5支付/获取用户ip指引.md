### 背景介绍

H5支付要求商户在统一下单接口中上传用户真实ip地址“spbill_create_ip”，为保证微信端获取的用户ip地址与商户端获取的一致，提供了以下获取用户ip的指引，希望对大家有所帮助。

### 没有代理的情况

在商户的前端接入层没有做代理的情况下获取ip的方式比较简单，直接获取'REMOTE_ADDR '即可。

![img](https://pay.weixin.qq.com/wiki/doc/api/img/chapter15_2.png)

### 有代理的情况

在有代理的情况下，因为要代替客户端去访问服务器，所以，当请求包经过反向代理后，在代理服务器这里这个IP数据包的IP包头做了修改，最终后端WEB服务器得到的数据包的头部源IP地址是代理服务器的IP地址。这样一来，后端服务器的程序就无法获取用户的真实ip。

nginx有代理的情况:

在nginx中配置中加入

```
proxy_set_header Host $host;

proxy_set_header X-Real-IP $remote_addr;

proxy_set_header X-Real-Port $remote_port;

proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;

 

Apache有代理的情况：

vi /usr/local/apache/conf/httpd.conf

Include conf/extra/httpd-remoteip.conf

vi /usr/local/apache/conf/extra/httpd-remoteip.conf

LoadModule remoteip_module modules/mod_remoteip.so

RemoteIPHeader X-Forwarded-For

RemoteIPInternalProxy 127.0.0.1
```



代码 示例

```
string GetClientIp(CgiInput* poInput) 

{ 

string client_ip = ""; 

string strClientIPList; 

GetHttpHeader("X-Forwarded-For", strClientIPList); 

 

if (strClientIPList.empty()) 

{ 

GetHttpHeader("X-Real-IP", strClientIPList); 

} 

 

if (!strClientIPList.empty()) 

{ 

size_t iPos = strClientIPList.find( "," ); 

if( iPos != std::string::npos ) 

{ 

client_ip = strClientIPList.substr( iPos ); 

} 

else 

{ 

client_ip = strClientIPList; 

} 

} 

 

if (client_ip.empty()) 

{ 

GetHttpHeader("PROXY_FORWARDED_FOR", strClientIPList); 

// 做下兼容 

if(strClientIPList.empty()) 

{ 

client_ip = getRemoteAddr(); 

} 

else 

{ 

size_t iPos = strClientIPList.find( "," ); 

if( iPos != std::string::npos ) 

{ 

client_ip = strClientIPList.substr( iPos ); 

} 

else 

{ 

client_ip = strClientIPList; 

} 

} 

} 

if(!MMPayCommFunc::IsIp(client_ip)) 

client_ip = getRemoteAddr(); 

return client_ip; 

} 
```

