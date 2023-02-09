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
    """\srt="+({time}\d{13})""",
    """\sduser="+({user}[^"]+)""",
    """\sduser="+[^@"]+@({email_domain}[^".]+)""",
    """\sdestinationServiceName ="({app}[^"]+)"""",
    """\sapp="({app}[^"]+)"""",
    """\srequestClientApplication=({user_agent}.+?)\s+rt=""",
    """\sdst="+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\ssrc="+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\soutcome="+({result}[^"]+)""",
    """\sdpriv="+({privileges}[^"]+)""",
  ]


}
```