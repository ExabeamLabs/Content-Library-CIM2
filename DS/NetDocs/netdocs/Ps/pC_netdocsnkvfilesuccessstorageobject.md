#### Parser Content
```Java
{
Name = "netdocs-n-kv-file-success-storageobject"
Vendor = "NetDocs"
Product = "NetDocs"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""<activity date=""""
"""<user id=""""
"""<storageObject"""
"""host=""""
"""name=""""
]
Fields = [
"""activity date="+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"+\sname"""
"""name="+({access}[^"]+)"+\shost"""
"""host="+({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""""
"""host="+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
"""name="+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"+\smemberType"""
"""user\sid="+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"+\sname"""
"""name="+({src_file_name}[^"]+)"+\s(version|size)"""
"""size="+({bytes}\d+)"+\sfileExtension"""
"""fileExtension="+({src_file_ext}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```