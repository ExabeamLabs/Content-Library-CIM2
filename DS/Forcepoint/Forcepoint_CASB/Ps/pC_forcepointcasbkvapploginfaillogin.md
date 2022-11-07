#### Parser Content
```Java
{
Name = forcepoint-casb-kv-app-login-fail-login
  ParserVersion = v1.0.0
  Vendor = Forcepoint
  Product = Forcepoint CASB
  TimeFormat = "epoch"
  Conditions = [ "CEF", "Skyfence", """|Activity|""", """reason="login"""" ]
  Fields = [
    """\sdvc="+({host}[^"]+)""",
    """\sdvchost="+({host}[^"]+)""",
    """\srt="+({time}\d+)""",
    """\sduser="+({user}[^"]+)""",
    """\sduser="+[^@"]+@({email_domain}[^".]+)""",
    """\sdestinationServiceName ="({app}[^"]+)"""",
    """\sapp="({app}[^"]+)"""",
    """\srequestClientApplication=({user_agent}.+?)\s+rt=""",
    """\sdst="+({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\ssrc="+({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\soutcome="+({result}[^"]+)""",
    """\sdpriv="+({privileges}[^"]+)""",
  ]


}
```