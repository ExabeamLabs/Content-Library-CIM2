#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-4769-7"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
""""event_code":4769"""
""""constrained-delegation":"""
""""disable-transited-check":"""
""""enc-tkt-in-skey":"""
]
Fields = [
""""host":"(::1|(((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({host}[\w\-\.]+))""""
""""src_ip":"(::1|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
""""dest_host":"({service_name}(\w+\/)?({dest_host}[^"]+?)(@({dest_domain}[^"]+))?)""""
""""time":({time}\d{13})"""
""""result_code":"({result_code}[^"]+)"""
""""user":(null|"({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
""""user":(null|"({user_upn}({user}[\w\.\-\!\#\^\~]{1,40}\$?)@[^"]+))"""
""""domain":"({domain}[^"]+)"""
""""event_code":({event_code}\d+)"""
]
ParserVersion = "v1.0.0"


}
```