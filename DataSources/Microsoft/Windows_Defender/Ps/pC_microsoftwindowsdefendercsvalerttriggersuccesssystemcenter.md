#### Parser Content
```Java
{
Name = microsoft-windowsdefender-csv-alert-trigger-success-systemcenter
  Vendor = Microsoft
  Product = Windows Defender
  TimeFormat = "MMM dd yyyy HH:mma"
  Conditions = [ """,SystemCenterEndpointProtection""" ]
  Fields = [
    """({time}\w+\s+\d+\s+\d\d\d\d\s+\d{1,2}:\d\d(AM|am|PM|pm))\,({alert_id}[^\,]+)\,({alert_name}[^\,]+)\,\w+\,({src_host}[^\,]+)\,[^,]+\,({additional_info}[^\,]+)\,(?:NA|({domain}[^\\]+))\\({user}[^\,]+)\,({alert_type}[^\,]+)\,({alert_severity}[^\,]+)\,SystemCenterEndpointProtection"""
  ]
  ParserVersion = "v1.0.0"


}
```