#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-modify-4717
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """4717""", """System security access was granted to an account""" ]
  Fields = [
    """<TimeCreated SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)\s+({host}[\w.\-]+)""",
    """({event_code}4717)""",
    """({event_name}System security access was granted to an account)""",
    """Subject:.*?Security ID:\s*(|({user_sid}.+?))\s*Account Name:\s*(|({user}.+?))\s*Account Domain:\s*(|({domain}.+?))\s*Logon ID:\s*(|({login_id}.+?))\s*Account Modified:""",
    """Account Modified:.*?Account Name:\s*(|(({dest_domain}\S[^\\\/]*?)?[\\\/]+)?({dest_user}[^\\\/]+?))\s*Access Granted:""",
    """Access Granted:.*?Access Right:\s*({access_type}.+?)\s*("|<|$)"""
  ]


}
```