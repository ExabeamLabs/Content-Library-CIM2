#### Parser Content
```Java
{
Name = sentinelone-v-cef-app-activity-success-mgmt
  Vendor = SentinelOne
  Product = Vigilance
  TimeFormat = "EEE, dd MMM yyy, HH:mm:ss z"
  Conditions = [ """CEF:""", """|SentinelOne|Mgmt|""", """accountName =""", """activityType=""", """notificationScope=""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d),\d{1,5}(\s+\S+){2}\s+CEF:""",
    """\srt=(#arcsightDate\()?({time}\w{3},\s\d\d\s\w{1,3}\s\d\d\d\d,\s\d\d:\d\d:\d\d\s\w{3})\)?""",
    """activityType=({event_code}\d+)\s\w+=""",
    """({app}SentinelOne)""",
    """\|SentinelOne\|Mgmt\|([^\|]+\|){2}({additional_info}[^\|]+?)\s*\|""",
    """\sMachine\s({dest_host}[\w\-\.]+)\|""",
    """\sosName =({os}[^=]+?)\s\w+="""
  ]
  ParserVersion = v1.0.0


}
```