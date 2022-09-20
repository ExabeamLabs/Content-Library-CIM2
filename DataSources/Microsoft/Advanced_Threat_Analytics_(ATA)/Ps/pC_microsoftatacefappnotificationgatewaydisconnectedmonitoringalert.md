#### Parser Content
```Java
{
Name = microsoft-ata-cef-app-notification-gatewaydisconnectedmonitoringalert
  Vendor = Microsoft
  Product = Advanced Threat Analytics (ATA)
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """|Microsoft|ATA|""", """|GatewayDisconnectedMonitoringAlert|""", """CEF:""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-][^\s]+)\s({host}[^\s]+)\sATA""",
    """CEF:([^\|]*\|){4}({alert_type}[^\|]+)\|({alert_name}[^\|]+)\|({alert_severity}[^\|]+)\|""",
    """msg=({additional_info}[^=]+?)\s+(\w+=|$)""",
    """msg=[^=]*?Gateway (?:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^\.\s]+))""",
    """cs1=({url}[^=]+?)\s*"*(\w+=|$)"""
  ]
  ParserVersion = "v1.0.0"


}
```