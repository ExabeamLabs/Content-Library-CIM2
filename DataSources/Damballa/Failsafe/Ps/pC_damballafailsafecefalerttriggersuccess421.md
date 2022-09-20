#### Parser Content
```Java
{
Name = damballa-failsafe-cef-alert-trigger-success-421
  ParserVersion = v1.0.0
  Vendor = Damballa
  Product = Failsafe
  TimeFormat = "epoch"
  Conditions = [ """|McAfee|ESM""", """|421-""" ]
  Fields = [
    """\srt=({time}\d+)""",
    """\|McAfee\|ESM\|[^|]+?\|[^|]+?\|({alert_name}[^|]+?)\|""",
    """\|McAfee\|ESM\|[^|]+?\|[^|]+?\|[^|]+?\|({alert_severity}[^|]+?)\|""",
    """\sdeviceTranslatedAddress=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sexternalId=({alert_id}\d+)""",
    """\sshost=({src_host}[^\s]+)""",
    """\ssrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sdst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\snitroObject_Type=({alert_type}.+?)\s+\w+=""",
    """\snitroURL=({additional_info}.+?)\s+\w+="""
  ]


}
```