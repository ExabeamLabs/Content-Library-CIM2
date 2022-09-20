#### Parser Content
```Java
{
Name = microsoft-windowsdefender-alert-trigger-success-systemcenterep
  Vendor = Microsoft
  Product = Windows Defender
  TimeFormat = "epoch_sec"
  Conditions = [ """vendor_product=SystemCenterEndpointProtection""" ]
  Fields = [
    """dest_name=({src_host}[^\s]+)\s""",
    """DetectionTime=({time}\d+)""",
    """user="*({domain}[^\\]+)?(\\)*({user}.+?)"*\starget""",
    """severity=({alert_severity}.+?)\s+category="*({alert_type}.+?)"*\saction""",
    """resourceid=({alert_id}[^\s]+)\s+""",
    """signature=({alert_name}[^\s]+)\s+""",
  ]
  ParserVersion = "v1.0.0"


}
```