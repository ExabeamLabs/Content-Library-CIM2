#### Parser Content
```Java
{
Name = sentinelone-v-cef-app-logout-success-newconsolelogout
  Vendor = SentinelOne
  Product = Vigilance
  TimeFormat = "EEE, dd MMM yyy, HH:mm:ss z"
  Conditions = [ """CEF:""", """|SentinelOne|Mgmt|""", """|SentinelOne - New Console Logout Activity""", """activityType=""", """notificationScope=""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d),\d{1,5}(\s+\S+){2}\s+CEF:""",
    """\srt=(#arcsightDate\()?({time}\w{3},\s\d\d\s\w{1,3}\s\d\d\d\d,\s\d\d:\d\d:\d\d\s\w{3})\)?""",
    """activityType=({event_code}\d+)\s\w+=""",
    """({app}SentinelOne)""",
    """\|SentinelOne\s-\sNew Console Logout Activity\s+\-\s({email_address}[^@\|]+@[^\.\|]+\.[^\|]+?)\s*\|""",
    """suser=({full_name}[^=]+?\s[^=]+?)\s\w+=""",
    """({event_name}New Console Logout Activity)"""
  ]
  ParserVersion = v1.0.0


}
```