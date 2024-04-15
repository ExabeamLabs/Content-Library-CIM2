#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-login-authentication"
Vendor = "Unix"
Product = "Unix"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
  """: Authentication <"""
  """> user: <"""
  """> account: <"""
  """> service: <"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[\+\-]\d+:\d+)\s+""",
  """\d\d:\d\d:\d\d(\.\S+)?\s(::ffff:)?({host}({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
  """({host}({dest_host}[\w\-\.]+))\ssu\[\d+\]:""",
  """({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\+\d\d:\d\d)\s({host}({dest_host}[\w\-\.]+))\s\w+\_\w+:""",
  """\sAuthentication\s*<({result}[^\s>]+)>"""
  """\sAuthentication\s*<({result}[^\s>]+)\s+({auth_method}[^>]+)>"""
  """\suser:\s*<({user}[^\s\>]+)>"""
  """\saccount:\s*<(({domain}[^\\\s>]+)\\+)?({account}[^\\\s>]+)>"""
  """\sservice:\s*<({event_code}[^>]+)>"""
  """Caused by:\s*({failure_reason}[^\s\(:>]+)"""
]
DupFields = [ "account->dest_user" ]
ParserVersion = "v1.0.0"


}
```