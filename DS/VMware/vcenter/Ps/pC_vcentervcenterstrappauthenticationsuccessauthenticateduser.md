#### Parser Content
```Java
{
Name = "vcenter-vcenter-str-app-authentication-success-authenticateduser"
  ParserVersion = "v1.0.0"
  Vendor = "VMware"
  Product = "vCenter"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSS"
  Conditions = [ """VMCACheckAccessKrb:""","""Authenticated user""" ]
  Fields =[
    """({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+)""",
    """VMCACheckAccessKrb:\s*({result}Authenticated)\suser\s(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s]+)))""",
    """\s\d{4}[^\s]+\s({host}[^\s]+)\s""",
  ]


}
```