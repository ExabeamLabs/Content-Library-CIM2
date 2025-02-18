#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-notification-4793
  Vendor = Microsoft
  ParserVersion = "v1.0.0"
  Product = Event Viewer - Security
  TimeFormat =  "MMM dd HH:mm:ss yyyy"
  Conditions = [ """The Password Policy Checking API was called""" ]
  Fields = [
    """\Wrt=({time}\d+)""",
    """({event_name}The Password Policy Checking API was called)""",
    """({event_code}4793)""",
    """"(?i)Computer(Name)?":\s*"({host}[^"]+)""""
    """\WComputerName:\s*(::ffff:)?({host}[\w\-.]+)""",
    """({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+)""",
    """(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d+:\d+:\d+ \d+)"""
    """\d+\s*\d+:\d+:\d+\s+(::ffff:)?(am|pm|\d{4}|({host}[\w\-.]+))\s""",
    """Security ID:\s*(SYSTEM|({user_sid}\S+))""",
    """Account Name:\s*(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:""",
    """Account Domain:\s*(NT Service|({domain}[^\s]+))\s+Logon ID:""",
    """Logon ID:\s*({login_id}\S+)\s+Additional Information:""",
    """Status Code:\s*({result}[^\s",]+)"""
 ]


}
```