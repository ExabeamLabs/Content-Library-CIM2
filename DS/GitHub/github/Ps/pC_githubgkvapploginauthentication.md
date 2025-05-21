#### Parser Content
```Java
{
Name = "github-g-kv-app-login-authentication"
  Vendor = "GitHub"
  Product = "GitHub"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """github_auth"""
    """GitHub::Authentication"""
    """from="""
  ]
  Fields = [
    """({host}[\w.\-]+)\s+github_auth:"""
    """\Wlogin=(nil|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^\s=]+))?)(\s+\w+=|\s*$)"""
    """\Wrepo=(nil|({object}.+?)(.git)?)(\s+\w+=|\s*$)"""
    """\Waction=({operation}[^\s]+?)(\s+\w+=|\s*$)"""
    """\Wprotocol=({protocol}[^\s]+)"""
    """({app}github)"""
    """\Wat=({result}.+?)(\s+\w+=|\s*$)"""
    """\Wmessage=\"({failure_reason}[^\"]+)\".*?\sat=failure"""
    """\Wip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """\Wuser_agent=\"({user_agent}[^\"]+)\""""
  ]
  ParserVersion = "v1.0.0"


}
```