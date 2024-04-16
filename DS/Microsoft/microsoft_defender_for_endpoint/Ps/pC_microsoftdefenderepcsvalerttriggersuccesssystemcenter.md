#### Parser Content
```Java
{
Name = microsoft-defenderep-csv-alert-trigger-success-systemcenter
  Vendor = Microsoft
  Product = Microsoft Defender for Endpoint
  TimeFormat = ["MMM dd yyyy HH:mma", "MMM dd yyyy  H:mma"]
  Conditions = [ """,SystemCenterEndpointProtection""" ]
  Fields = [
    """({time}\w+\s+\d+\s+\d\d\d\d\s+\d{1,2}:\d\d(AM|am|PM|pm))\,({alert_id}[^\,]+)\,({alert_name}[^\,]+)\,\w+\,({src_host}[^\,]+)\,[^,]+\,({additional_info}[^\,]+)\,(?:NA|({domain}[^\\]+))\\({user}[\w\.\-]{1,40}\$?)\,({alert_type}[^\,]+)\,({alert_severity}[^\,]+)\,SystemCenterEndpointProtection"""
  ]
  ParserVersion = "v1.0.0"


}
```