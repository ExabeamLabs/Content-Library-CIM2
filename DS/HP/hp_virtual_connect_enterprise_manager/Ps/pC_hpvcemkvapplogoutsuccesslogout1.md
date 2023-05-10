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
     """User Operation : User LogOut \(?({auth_type}\w+)\s({domain}[^\\]+)\\({user}[^@]+)@({src_ip}[A-Fa-f:\d.]+)\)?""",
     """({event_name}User LogOut)""",
     """({app}VCM)"""
  ]


}
```