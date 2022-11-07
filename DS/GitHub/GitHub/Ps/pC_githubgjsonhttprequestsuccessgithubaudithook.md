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
    """"start":({time}\d+),""",
    """({host}\S+)\s+github_audit:""",
    """"+actor"+:"+({user}[^"]+)""",
    """"+action"+:"+({operation}[^"]+)""",
    """"+repo"+:"+({resource}[^"]+)""",
    """({object}"+hook_id"+:[^,]+)""",
    """"+actor_ip"+:"+({src_ip}[^"]+)""",
    """"+config"+:\{({additional_info}.+?)\

}
```