#### Parser Content
```Java
{
Name = damballa-failsafe-cef-alert-trigger-success-421
  ParserVersion = v1.0.0
  Vendor = Damballa
  Product = Damballa Failsafe
  TimeFormat = "epoch"
  Conditions = [ """|McAfee|ESM""", """|421-""" ]
  Fields = [
    """\srt=({time}\d{13})""",
    """\|McAfee\|ESM\|[^|]+?\|[^|]+?\|({alert_name}[^|]+?)\|""",
    """\|McAfee\|ESM\|[^|]+?\|[^|]+?\|[^|]+?\|({alert_severity}[^|]+?)\|""",
    """\sdeviceTranslatedAddress=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sexternalId=({alert_id}\d+)""",
    """\sshost=({src_host}[^\s]+)""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\snitroObject_Type=({alert_type}.+?)\s+\w+=""",
    """\snitroURL=({additional_info}.+?)\s+\w+="""
  ]


}
```