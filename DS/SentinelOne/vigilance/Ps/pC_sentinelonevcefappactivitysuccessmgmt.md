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
    """\srt=(#arcsightDate\()?({time}\w{3

}
```