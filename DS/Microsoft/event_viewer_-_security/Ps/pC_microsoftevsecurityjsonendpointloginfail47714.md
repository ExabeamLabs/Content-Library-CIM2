#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-fail-4771-4"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
  """"event_code":4771"""
  """"constrained-delegation":"""
  """"disable-transited-check":"""
  """"enc-tkt-in-skey":"""
]
Fields = [
  """"time":({time}\d{13})"""
  """"host":"(::1|({host}[a-fA-F:\d.]+))"""
  """"src_ip":"(::1|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
  """"result_code":"({result_code}[^"]+)"""
  """"user":(null|"({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """"user":(null|"({email_address}({user}[\w\.\-\!\#\^\~]{1,40}\$?)@[^"]+))"""
  """"domain":"({domain}[^"]+)"""
  """"event_code":({event_code}\d+)"""
]
DupFields = [
  "result_code->failure_code"
]
ParserVersion = "v1.0.0"


}
```