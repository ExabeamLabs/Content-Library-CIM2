#### Parser Content
```Java
{
Name = crowdstrike-falcon-leef-app-login-falconhost
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """LEEF:""", """|CrowdStrike|FalconHost|""", """cat=AuthActivityAuditEvent""" ]
  Fields = [
    """\WdevTime=({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)""",
    """\WusrName =({user}[^=@]+?)(@({domain}[^@]+?))?(\s*\||\s+\w+=|\s*$|\s*")""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wsuccess=({result}\w+).+?\s*(\||\w+=|$)""",
    """({app}FalconHost)""",
    """"aid":"({aid}[^"]+)"""
  ]
  DupFields = ["domain->email_domain"]
  ParserVersion = "v1.0.0"


}
```