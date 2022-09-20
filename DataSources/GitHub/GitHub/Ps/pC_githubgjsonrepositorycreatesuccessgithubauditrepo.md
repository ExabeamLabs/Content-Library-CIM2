#### Parser Content
```Java
{
Name = github-g-json-repository-create-success-githubauditrepo
  ParserVersion = v1.0.0
  Vendor = GitHub
  Product = GitHub
  TimeFormat = "epoch"
  Conditions = [ """github_audit""", """action":"repo""" ]
  Fields = [
    """"created_at":({time}\d+),""",
    """"start":({time}\d+),""",
    """({host}\S+)\s+github_audit:""",
    """"+actor"+:"+({user}[^"]+)""",
    """"+action"+:"+({operation}[^"]+)""",
    """"+actor_ip"+:"+({src_ip}[^"]+)""",
    """"+repo"+:"+({object}[^"]+)""",
    """({app}github)"""
  ]


}
```