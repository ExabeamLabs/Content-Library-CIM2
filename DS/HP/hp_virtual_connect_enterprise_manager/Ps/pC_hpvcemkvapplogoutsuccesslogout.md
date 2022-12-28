#### Parser Content
```Java
{
Name = hp-vcem-kv-app-logout-success-logout
  ParserVersion = "v1.0.0"
  Vendor = HP
  Product = HP Virtual Connect Enterprise Manager
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """vcmd:""", """VCM user logout :""" ]
  Fields = [
     """\d\d:\d\d:\d\d\s({host}\S+)\svcmd:""",
     """VCM user logout : ({auth_type}\w+)\s({domain}[^\\]+)\\({user}[^@]+)@({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """({event_name}user logout)""",
     """({app}VCM)"""
  ]


}
```