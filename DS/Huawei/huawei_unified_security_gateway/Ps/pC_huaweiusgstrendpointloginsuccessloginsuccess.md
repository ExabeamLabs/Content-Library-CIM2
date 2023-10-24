#### Parser Content
```Java
{
Name = huawei-usg-str-endpoint-login-success-loginsuccess
  Vendor = Huawei
  Product = Huawei Unified Security Gateway
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """HTTPD""", """ User """, """ login succeeded""" ]
  Fields = [
     """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d),\S+\s+({host}[\w\.\-]+)""",
     """User ({user}[\w\.\-]{1,40}\$?)\(""",
     """IP:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """\slogin ({result}succeeded)""",
  ]
  ParserVersion = "v1.0.0"


}
```