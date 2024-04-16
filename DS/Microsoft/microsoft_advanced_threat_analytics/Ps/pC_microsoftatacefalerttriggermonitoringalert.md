#### Parser Content
```Java
{
Name = microsoft-ata-cef-alert-trigger-monitoringalert
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  Product = Microsoft Advanced Threat Analytics
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = [ """|Microsoft|ATA|""", """|GatewayOverloadedNetworkActivitiesMonitoringAlert|""", """CEF:""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-][^\s]+)\s({host}[^\s]+)\sATA""",
    """CEF:([^\|]*\|){4}({alert_type}[^\|]+)\|({alert_name}[^\|]+)\|({alert_severity}[^\|]+)\|""",
    """msg=({additional_info}[^=]+?)\s+(\w+=|$)""",
    """msg=[^=]*?Gateway, (?:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^\.\s]+)),""",
    """cs1=({url}[^=]+?)\s*"*(\w+=|$)"""
  ]


}
```