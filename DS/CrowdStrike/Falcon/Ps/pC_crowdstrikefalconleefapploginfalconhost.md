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
    """\Wsrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\Wsuccess=({result}.+?)\s*(\||\w+=|$)""",
    """({app}FalconHost)""",
  ]
  DupFields = ["domain->email_domain"]
  ParserVersion = "v1.0.0"


}
```