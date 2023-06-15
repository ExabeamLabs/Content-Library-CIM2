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
    """"start":({time}\d{13}),""",
    """({host}\S+)\s+github_audit:""",
    """"+actor"+:"+({user}[^"]+)""",
    """"+action"+:"+({operation}[^"]+)""",
    """"+actor_ip"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"+repo"+:"+({object}[^"]+)""",
    """({app}github)"""
  ]


}
```