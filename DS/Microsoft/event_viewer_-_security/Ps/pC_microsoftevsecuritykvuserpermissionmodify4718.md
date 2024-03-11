#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-permission-modify-4718
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """4718""", """System security access was removed from an account""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)\s+({host}[\w.\-]+)""",
    """({event_code}4718)""",
    """({event_name}System security access was removed from an account)""",
    """Subject:.*?Security ID:\s*(|({user_sid}.+?))\s*Account Name:\s*(|({user}.+?))\s*Account Domain:\s*(|({domain}.+?))\s*Logon ID:\s*(|({login_id}.+?))\s*Account Modified:""",
    """Account Modified:.*?Account Name:\s*(|(({dest_domain}\S[^\\\/]*?)?[\\\/]+)?({dest_user}[^\\\/]+?))\s*Access Removed:""",
    """Access Removed:.*?Access Right:\s*({access_type}.+?)\s*("|$)""",
  ]


}
```