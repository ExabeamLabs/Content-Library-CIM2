#### Parser Content
```Java
{
Name = "github-g-json-app-login-fail-failedlogin"
  Vendor = "GitHub"
  Product = "GitHub"
  TimeFormat = "epoch"
  Conditions = [
    """failed_login"""
    """github_audit"""
  ]
  Fields = [
    """\"start\":({time}\d{13}),"""
    """\"+@timestamp\"+:({time}\d+)"""
    """({host}\S+)\s+github_audit:"""
    """\"+host\"+:\"+({host}[^\"]+)"""
    """\"+action\"+:\"+({operation}[^\"]+)"""
    """\"+user\"+:\"+({user}[^\"]+)"""
    """\"+actor_ip\"+:\"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """({app}github)"""
  ]
  ParserVersion = "v1.0.0"


}
```