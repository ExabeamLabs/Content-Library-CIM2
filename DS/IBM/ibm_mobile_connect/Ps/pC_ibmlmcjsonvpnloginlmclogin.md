#### Parser Content
```Java
{
Name = "ibm-lmc-json-vpn-login-lmclogin"
Vendor = "IBM"
Product = "IBM Mobile Connect"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""action":"lmc_login_"""
""""userID":""""
""""srcIP":"""
]
Fields = [
""""@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
"""({host}[\w\-.]+)\s+\{""""
""""srcIP":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""dstIP":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""""action":"({action}[^"]+)"""
""""userID":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
]
DupFields = [
"user->account"
]
ParserVersion = "v1.0.0"


}
```