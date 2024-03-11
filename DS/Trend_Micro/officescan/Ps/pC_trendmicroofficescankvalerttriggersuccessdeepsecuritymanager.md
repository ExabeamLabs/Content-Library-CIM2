#### Parser Content
```Java
{
Name = trendmicro-officescan-kv-alert-trigger-success-deepsecuritymanager
  ParserVersion = "v1.0.0"
  Conditions = [ """|Trend Micro|Deep Security Manager|""","""cat=""" ]

trendmicro-security-alert = {
  Vendor = Trend Micro
  Product = OfficeScan
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """\Wcat=({threat_category}.+?)\s*(\w+=|$)""",
    """\Wname=({alert_name}.+?)\s*(\w+=|$)""",
    """\Wsev=({alert_severity}\d+)""",
    """\Wdvchost=({host}.+?)\s*(\w+=|$)""",
    """\WfilePath=({malware_url}.+?)\s*(\w+=|$)""",
        ]
  DupFields = [ "threat_category->alert_type", "host->src_host" 
}
```