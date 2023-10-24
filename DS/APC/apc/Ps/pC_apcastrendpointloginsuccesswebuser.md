#### Parser Content
```Java
{
Name = "apc-a-str-endpoint-login-success-webuser"
  ParserVersion = "v1.0.0"
  Vendor = "APC"
  Product = "APC"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
""" Web user """ 
""" logged in from """ 
]
  Fields = [
"""<\d+>(\w+\s+\d+\s+\d\d:\d\d:\d\d)\s+({host}[\w.\-]+)\s"""
"""Web user '({user}[\w\.\-]{1,40}\$?)'"""
"""\slogged in from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\.?\s+"""
  ]
  DupFields = [ "host->dest_host" ]


}
```