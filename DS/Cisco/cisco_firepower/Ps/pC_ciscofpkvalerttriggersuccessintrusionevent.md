#### Parser Content
```Java
{
Name = cisco-fp-kv-alert-trigger-success-intrusionevent
  Vendor = Cisco
  Product = Cisco Firepower
  TimeFormat = ["dd MMMM yyyy HH:mm:ss","dd MMM yyyy HH:mm:ss"]
  Conditions = [ """DeviceType=Estreamer""", """recordType=INTRUSION_EVENT_RECORD3""" ]
  Fields = [
      """\stimestamp=({time}\d\d \w{3} \d{4} \d\d:\d\d:\d\d)""",
      """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
      """\sDeviceAddress=({host}[^\s]+)""",
      """\seventId=({alert_id}\d+)""",
      """\ssourceAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """\sdestinationAddress=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """\spriority.name=({alert_severity}[^\s]+)""",
      """\sclassification.description=({alert_name}.+?)\sclassification""",
      """\sclassification.name=({alert_type}.+?)\sclassification"""
  ]
  ParserVersion = "v1.0.0"


}
```