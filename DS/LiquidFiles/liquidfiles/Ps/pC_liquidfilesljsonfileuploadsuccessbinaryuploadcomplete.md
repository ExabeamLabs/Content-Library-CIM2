#### Parser Content
```Java
{
Name = "liquidfiles-l-json-file-upload-success-binaryuploadcomplete"
Vendor = "LiquidFiles"
Product = "LiquidFiles"
Conditions = [
"""liquidfiles["""
""""message":"Binary Upload Complete""""
]
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Fields = [
""""hostname":"({host}[^"]+)""""
""""filename":"({file_name}[^"]+(\.)({file_ext}[^"]+))""""
""""ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""user_id":"(n/a|({user}[^"]+?))""""
""""message":"({event_name}[^:"]+)"""
"""({app}liquidfiles)"""
""""username":"(({email_address}[^@"]+@[^\.]+\.[^"]+)|({user}[^"]+))""""
]
ParserVersion = "v1.0.0"


}
```