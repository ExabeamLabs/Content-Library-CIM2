#### Parser Content
```Java
{
Name = github-g-json-user-invite-success-org
  ParserVersion = v1.0.0
  Vendor = GitHub
  Product = GitHub
  TimeFormat = "epoch"
  Conditions = [ """github_audit""", """action":""", """"org""" ]
  Fields = [
    """"start":({time}\d{13}),""",
    """({host}\S+)\s+github_audit:""",
    """"+actor"+:\s*"+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """"+user"+:\s*"+({resource}[^"]+)""",
    """"+action"+:\s*"+({operation}[^"]+)""",
    """"+actor_ip"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"+org"+:\s*"+({object}[^"]+)""",
    """({app}github)"""
  ]


}
```