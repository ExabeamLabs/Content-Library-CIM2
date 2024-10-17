#### Parser Content
```Java
{
Name = sentinelone-v-cef-app-activity-success-usercreatedrole
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|SentinelOne|Mgmt|""", """|User created role|""", """activityType=""", """notificationScope=""" ]
  Fields = ${SentinelOneParsersTemplates.sentinelone-vigilance-app-events.Fields}[
    """({operation}User created role)"""
  ]

sentinelone-vigilance-app-events {
  Vendor = SentinelOne
  Product = Vigilance
  TimeFormat = ["EEE, dd MMM yyyy, HH:mm:ss z","EEE, dd MMM yyyy, HH:mm:ss Z"]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d),\d{1,5}(\s+\S+){2}\s+CEF:""",
    """\srt=(#arcsightDate\()?({time}\w{3},\s\d\d\s\w{1,3}\s\d\d\d\d,\s\d\d:\d\d:\d\d\s\w{3})\)?""",
    """activityType=({event_code}\d+)\s\w+=""",
    """({app}SentinelOne)""",
    """suser=(({full_name}[^=]+?\s[^=]+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s\w+="""
  
}
```