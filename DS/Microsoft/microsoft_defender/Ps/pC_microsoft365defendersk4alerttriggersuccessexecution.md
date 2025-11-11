#### Parser Content
```Java
{
Name = "microsoft-365defender-sk4-alert-trigger-success-execution"
Product = "Microsoft Defender"
Conditions = [
""""category":""""
"""Execution"""
""""title":""""
""""vendor":""""
"""Microsoft"""
""""provider":""""
"""Microsoft 365 Defender"""
]
ParserVersion = "v1.0.0"

cef-atp-alert = {
  Vendor = Microsoft
  Product = Azure ATP
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """CEF:?([^\|]*\|){4}({alert_type}[^\|]+)\|({alert_name}[^\|]+)\|({alert_severity}[^\|]+)\|""",
    """\WexternalId=({event_code}\d+)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """\Wstart=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """\Wapp=({service_name}.+?)\s+(\w+=|$)""",
    """\Wshost=(({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})|({src_host}[\w\-.]+))""",
    """\Wmsg=({additional_info}.+?)\s+(\w+=|$)""",
    """\Wcs1=({url}.+?)\s+(\w+=|$).+?cs1Label=url""",
    """\Wcs1Label=url.*?\Wcs1=({url}.+?)\s+(\w+=|$)""",
    """\Wsuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s""",
    """\Wcs2=({incident_status}[^\s]+)""",
  
}
```