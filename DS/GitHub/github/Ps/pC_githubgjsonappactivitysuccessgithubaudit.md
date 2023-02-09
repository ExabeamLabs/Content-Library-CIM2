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
    """"+real_ip"+:"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"+pubkey_fingerprint"+:"+({fingerprint}[^"]+)""",
    """({app}github)"""
  ]


}
```