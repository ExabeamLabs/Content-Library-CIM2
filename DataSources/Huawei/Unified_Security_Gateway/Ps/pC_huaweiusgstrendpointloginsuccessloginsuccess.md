#### Parser Content
```Java
{
Name = huawei-usg-str-endpoint-login-success-loginsuccess
  Vendor = Huawei
  Product = Unified Security Gateway
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """HTTPD""", """ User """, """ login succeeded""" ]
  Fields = [
     """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d),\S+\s+({host}[\w\.\-]+)""",
     """User ({user}[^\(]+)\(""",
     """IP:({src_ip}[a-fA-F\d.:]+)""",
     """\slogin ({result}succeeded)""",
  ]
  ParserVersion = "v1.0.0"


}
```