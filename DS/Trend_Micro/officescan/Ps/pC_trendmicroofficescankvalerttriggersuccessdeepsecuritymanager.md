#### Parser Content
```Java
{
Name = trendmicro-officescan-kv-alert-trigger-success-deepsecuritymanager
  ParserVersion = "v1.0.0"
  Conditions = [ """|Trend Micro|Deep Security Manager|""","""cat=""" ]

trendmicro-security-alert = { 
  Vendor = Trend Micro
  Product = OfficeScan
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[\+\-]\d\d:\d\d)\s\S+""",
    """\Wcat=({alert_type}({threat_category}.+?))\s*(\w+=|$)""",
    """\Wname=({alert_name}.+?)\s*(\w+=|$)""",
    """\Wsev=({alert_severity}\d+)""",
    """\d\d:\d\d:\d\d\S+\s({src_host}({host}[\w\-\.]+))""",
    """\Wdvchost=({src_host}({host}.+?))\s*(\w+=|$)""",
    """\WfilePath=({malware_url}.+?)\s*(\w+=|$)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s*(\w+=|$)""",
    """target=(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-\.]+))\s*(\w+=|$)"""
        
}
```