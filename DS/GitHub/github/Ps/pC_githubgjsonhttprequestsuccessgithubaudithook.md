#### Parser Content
```Java
{
Name = github-g-json-http-request-success-githubaudithook
  ParserVersion = v1.0.0
  Vendor = GitHub
  Product = GitHub
  TimeFormat = "epoch"
  Conditions = [ """github_audit""", """action":"hook""" ]
  Fields = [
    """"start":({time}\d{13}),""",
    """({host}\S+)\s+github_audit:""",
    """"+actor"+:"+({user}[^"]+)""",
    """"+action"+:"+({operation}[^"]+)""",
    """"+repo"+:"+({resource}[^"]+)""",
    """({object}"+hook_id"+:[^,]+)""",
    """"+actor_ip"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"+config"+:\{({additional_info}.+?)\

}
```