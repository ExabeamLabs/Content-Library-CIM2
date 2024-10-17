#### Parser Content
```Java
{
Name = "vmware-carbonblack-sk4-app-login-success-loggedinsuccessfully"
Vendor = "VMware"
Product = "Carbon Black CES"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""destinationServiceName =CB Defense"""
""""loginName":"""
"""logged in successfully"""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
""""loginName":"(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({email_address}[^"]+@[^"]+))""""
"""clientIp":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""description":"({event_name}[^"]+)"""
"""({app}CB Defense)"""
]
ParserVersion = "v1.0.0"


}
```