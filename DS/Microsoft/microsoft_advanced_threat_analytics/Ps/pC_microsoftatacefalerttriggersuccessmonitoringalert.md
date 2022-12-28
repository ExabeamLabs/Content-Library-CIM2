#### Parser Content
```Java
{
Name = microsoft-ata-cef-alert-trigger-success-monitoringalert
Vendor = Microsoft
Product = Microsoft Advanced Threat Analytics
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """|Microsoft|ATA|"""
  """|CenterDatabaseDisconnectedMonitoringAlert|"""
]
Fields = [
  """CEF:([^\|]*\|){4}({alert_type}[^\|]+)\|({alert_name}[^\|]+)\|({alert_severity}[^\|]+)\|"""
  """\WexternalId=({alert_id}\d+)"""
  """\Wapp=({service_name}.+?)\s+(\w+=|$)"""
  """\Wmsg=({additional_info}.+?)\s+(\w+=|$)"""
  """\Wsuser=(?:(({last_name}[\w\']+), ({first_name}\w+))|({user}[^\s]+))\s+(\w+=|$)"""
  """\Wshost=(?:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w.\-]+))\s+(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```