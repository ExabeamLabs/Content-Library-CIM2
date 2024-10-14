#### Parser Content
```Java
{
Name = microsoft-defenderep-kv-alert-trigger-success-systemcenterep-1
  Vendor = Microsoft
  Product = Microsoft Defender for Endpoint
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """vendor_product=SystemCenterEndpointProtection""" ]
  Fields = [
    """dest_name=({src_host}[^\s]+)\s""",
    """DetectionTime=({time}\d+)""",
    """user="*({domain}[^\\]+)?(\\)*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"*\starget""",
    """severity=({alert_severity}.+?)\s+category="*({alert_type}.+?)"*\saction""",
    """resourceid=({alert_id}[^\s]+)\s+""",
    """signature=({alert_name}[^\s]+)\s+""",
  ]
  ParserVersion = "v1.0.0"


}
```