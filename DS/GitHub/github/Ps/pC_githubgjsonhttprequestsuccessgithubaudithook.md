#### Parser Content
```Java
{
Name = github-g-json-http-request-success-githubaudithook
  ParserVersion = v1.0.0
  Vendor = GitHub
  Product = GitHub
  TimeFormat = "epoch"
  Conditions = [ """github_audit""", """action":""", """"hook""" ]
  Fields = [
    """"start":\s*({time}\d{13}),""",
    """({host}\S+)\s+github_audit:""",
    """"+actor"+:\s*"+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """"+action"+:\s*"+({operation}[^"]+)""",
    """"+repo"+:\s*"+({resource}[^"]+)""",
    """({object}"+hook_id"+:[^,]+)""",
    """"+actor_ip"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"+config"+:\{({additional_info}.+?)\},""",
    """({app}github)"""
  ]


}
```