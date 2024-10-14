#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-permission-modify-4718
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
  Conditions = [ """4718""", """System security access was removed from an account""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)\s+({host}[\w.\-]+)""",
    """<TimeCreated SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\dZ)""""
    """({event_code}4718)""",
    """({event_name}System security access was removed from an account)""",
    """Subject:.*?Security ID:\s*(|({user_sid}.+?))\s*Account Name:\s*(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*Account Domain:\s*(|({domain}.+?))\s*Logon ID:\s*(|({login_id}.+?))\s*Account Modified:""",
    """Account Modified:.*?Account Name:\s*(|(({dest_domain}\S[^\\\/]*?)?[\\\/]+)?(({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)|({dest_user_sid}[^\s]+)))\s*Access Removed:""",
    """Access Removed:.*?Access Right:\s*({access_type}.+?)\s*("|<|$)""",
  ]


}
```