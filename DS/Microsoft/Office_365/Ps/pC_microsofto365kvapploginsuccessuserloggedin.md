#### Parser Content
```Java
{
Name = microsoft-o365-kv-app-login-success-userloggedin
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Office 365
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """SESSID=""", """RESULTCODE=""", """WORKLOAD=""", """COMMAND=UserLoggedIn""", """OBJECT=""" ]
  Fields = [
    """\sTS=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """USER=(Unknown|({email_address}[^@\s]+@[^\s\.]+?\.[^\s]+?)|({user}[^\s@]+)(@({domain}[^\s]+))?)\s+\w+=""",
    """DOMAIN=(|({domain}[^\s]+?))\s+\w+=""",
    """WORKLOAD=({app}[^=]+?)\s+\w+=""",
    """COMMAND=({event_name}[^=]+?)\s+\w+=""",
    """OBJECT=(Unknown|({object}[^=]+?))\s+\w+=""",
    """SIP=({src_ip}[a-fA-F\d:.]+)""",
    """RESULTCODE=({result}[^=]+?)\s+\w+=""",
    """USERAGENT=\s*(|({user_agent}[^\n]+?))\s*(\w+=|$)"""
  ]


}
```