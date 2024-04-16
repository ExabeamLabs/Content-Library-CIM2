#### Parser Content
```Java
{
Name = sentinelone-v-cef-alert-trigger-success-activethreat
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|SentinelOne|Mgmt|""", """|New active threat""", """activityType=""", """notificationScope=""" ]

sentinelone-vigilance-alerts {
    Vendor = SentinelOne
    Product = Vigilance
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSS","yyyy-MM-dd HH:mm:ss.SSSSSS"]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d),\d{1,5}(\s+\S+){2}\s+CEF:""",
      """\srt=({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d{1,6})\s""",
      """\smachine\s({dest_host}[\w\-\.]+)\|""",
      """activityType=({event_code}\d+)\s\w+=""",
      """\|SentinelOne\|Mgmt\|([^\|]+\|){2}({alert_name}[^\|\-]+)\s\-""",
      """\|SentinelOne\|Mgmt\|([^\|]+\|){3}({alert_severity}\d{1,2})""",
      """activityID=({alert_id}\d+)\s\w+=""",
      """\scat=({alert_type}\S+)""",
      """fileHash=({hash_sha1}[^\s]+)\s\w+=""",
      """filePath=({file_path}({file_dir}[^=]+?)[\\\/]+({file_name}[^=\/\\]+?(\.({file_ext}[^=\/\\]+))?))\s\w+="""
    
}
```