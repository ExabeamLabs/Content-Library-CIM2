#### Parser Content
```Java
{
Name = microsoft-atp-cef-alert-trigger-success-directoryservicesroguereplication
  ParserVersion = v1.0.0
  Product = Advanced Threat Protection
  Conditions = [ """CEF""", """|Microsoft|Azure ATP|""", """|DirectoryServicesRogueReplicationSecurityAlert|""" ]

cef-atp-alert = {
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """CEF:?([^\|]*\|){4}({alert_type}[^\|]+)\|({alert_name}[^\|]+)\|({alert_severity}[^\|]+)\|""",
    """\WexternalId=({alert_id}\d+)""",
    """\Wstart=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """\Wapp=({service_name}.+?)\s+(\w+=|$)""",
    """\Wshost=(({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})|({src_host}[\w\-.]+))""",
    """\Wmsg=({additional_info}.+?)\s+(\w+=|$)""",
    """\Wcs1=({url}.+?)\s+(\w+=|$).+?cs1Label=url""",
    """\Wcs1Label=url.*?\Wcs1=({url}.+?)\s+(\w+=|$)""",
    """\Wsuser=({user}[^\s]+)\s""",
    """\Wcs2=({result}[^\s]+)""",
  
}
```