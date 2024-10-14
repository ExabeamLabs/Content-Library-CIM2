#### Parser Content
```Java
{
Name = "liquidfiles-l-json-file-download-success-downloadsuccess"
Conditions = [
"""liquidfiles["""
""""message":"Attachment Downloaded Successfully""""
""""filename":""""
]
Vendor = "LiquidFiles"
Product = "LiquidFiles"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Fields = [
""""hostname":"({host}[^"]+)""""
""""filename":"({file_name}[^"]+(\.)({file_ext}[^"]+))""""
""""ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""user_id":"(n/a|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
""""message":"({event_name}[^:"]+)""""
"""({app}liquidfiles)"""
""""username":"(({email_address}[^@"]+@[^\.]+\.[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
]
ParserVersion = "v1.0.0"


}
```