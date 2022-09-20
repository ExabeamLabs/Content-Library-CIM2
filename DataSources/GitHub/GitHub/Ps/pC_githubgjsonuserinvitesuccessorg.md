#### Parser Content
```Java
{
Name = github-g-json-user-invite-success-org
  ParserVersion = v1.0.0
  Vendor = GitHub
  Product = GitHub
  TimeFormat = "epoch"
  Conditions = [ """github_audit""", """action":"org""" ]
  Fields = [
    """"start":({time}\d+),""",
    """({host}\S+)\s+github_audit:""",
    """"+actor"+:"+({user}[^"]+)""",
    """"+user"+:"+({resource}[^"]+)""",
    """"+action"+:"+({operation}[^"]+)""",
    """"+actor_ip"+:"+({src_ip}[^"]+)""",
    """"+org"+:"+({object}[^"]+)""",
    """({app}github)"""
  ]


}
```