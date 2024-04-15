#### Parser Content
```Java
{
Name = "microsoft-ata-cef-app-notification-gatewaystartfailuremonitoringalert"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Microsoft Advanced Threat Analytics"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """|Microsoft|ATA|""", """|GatewayStartFailureMonitoringAlert|""", """CEF:""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-][^\s]+)\s({host}[^\s]+)\sATA""",
    """CEF:([^\|]*\|){4}({alert_type}[^\|]+)\|({alert_name}[^\|]+)\|({alert_severity}[^\|]+)\|""",
    """msg=({additional_info}[^=]+?)\s+(\w+=|$)""",
    """msg=[^=]*?Gateway service on (?:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^\.\s]+))""",
    """cs1=({url}[^=]+?)\s*"*(\w+=|$)"""
  ]


}
```