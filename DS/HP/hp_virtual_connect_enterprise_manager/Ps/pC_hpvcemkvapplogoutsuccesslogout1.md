#### Parser Content
```Java
{
Name = hp-vcem-kv-app-logout-success-logout-1
  ParserVersion = "v1.0.0"
  Vendor = HP
  Product = HP Virtual Connect Enterprise Manager
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """vcmd:""", """User Operation : User LogOut""" ]
  Fields = [
     """\d\d:\d\d:\d\d\s({host}\S+)\svcmd:""",
     """User Operation : User LogOut \(?({auth_type}\w+)\s({domain}[^\\]+)\\({user}[\w\.\-]{1,40}\$?)@({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\)?""",
     """({event_name}User LogOut)""",
     """({app}VCM)"""
  ]


}
```