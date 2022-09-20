#### Parser Content
```Java
{
Name = huawei-usg-kv-vpn-logout-success-logout
  Vendor = Huawei
  Product = Unified Security Gateway
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """UM/""", """/LOGOUT""", """Source IP=""" ]
  Fields = [
     """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d),\S+\s+({host}[\w\.\-]+)""",
     """User Name =(?!\d+\.\d+\.\d+\.\d+)(?:unknown|(email_address}[^@,]+@[^@,]+)|({user}[^,]+)),""",
     """Source IP=({src_ip}[a-fA-F\d.:]+)""",
  ]


}
```