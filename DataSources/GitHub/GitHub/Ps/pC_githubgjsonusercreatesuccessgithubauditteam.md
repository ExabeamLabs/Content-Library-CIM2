#### Parser Content
```Java
{
Name = github-g-json-user-create-success-githubauditteam
  ParserVersion = v1.0.0
  Vendor = GitHub
  Product = GitHub
  TimeFormat = "epoch"
  Conditions = [ """github_audit""", """action":"team""" ]
  Fields = [
    """"start":({time}\d+),""",
    """({host}\S+)\s+github_audit:""",
    """"+actor"+:"+({user}[^"]+)""",
    """"+action"+:"+({operation}[^"]+)""",
    """"+user"+:"+({resource}[^"]+)""",
    """"+actor_ip"+:"+({src_ip}[^"]+)""",
    """"+team"+:"+({object}[^"]+)""",
    """"+repo"+:"+({resource}[^"]+)""",
    """({additional_info}"+ldap_mapped"+:[^,]+)""",
    """({app}github)"""
  ]


}
```