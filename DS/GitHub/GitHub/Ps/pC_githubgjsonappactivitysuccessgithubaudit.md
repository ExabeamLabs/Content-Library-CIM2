#### Parser Content
```Java
{
Name = github-g-json-app-activity-success-githubaudit
  ParserVersion = v1.0.0
  Vendor = GitHub
  Product = GitHub
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """repo_name""", """github_audit""" ]
  Fields = [
    """"+@timestamp"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"+hostname"+:"+({host}[^"]+)""",
    """"+repo_name"+:"+({object}[^"]+)""",
    """"+program"+:"+({operation}[^"]+)""",
    """"+user_login"+:"+({user}[^"]+)""",
    """"+real_ip"+:"+({src_ip}[^"]+)""",
    """"+pubkey_fingerprint"+:"+({fingerprint}[^"]+)""",
    """({app}github)"""
  ]


}
```