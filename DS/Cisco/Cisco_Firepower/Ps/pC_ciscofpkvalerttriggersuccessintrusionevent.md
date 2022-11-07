#### Parser Content
```Java
{
Name = cisco-fp-kv-alert-trigger-success-intrusionevent
  Vendor = Cisco
  Product = Cisco Firepower
  TimeFormat = "dd MMMM yyyy HH:mm:ss"
  Conditions = [ """DeviceType=Estreamer""", """recordType=INTRUSION_EVENT_RECORD3""" ]
  Fields = [
      """\stimestamp=({time}\d\d \w{3} \d{4} \d\d:\d\d:\d\d)""",
      """\sDeviceAddress=({host}[^\s]+)""",
      """\seventId=({alert_id}\d+)""",
      """\ssourceAddress=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """\sdestinationAddress=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """\spriority.name=({alert_severity}[^\s]+)""",
      """\sclassification.description=({alert_name}.+?)\sclassification""",
      """\sclassification.name=({alert_type}.+?)\sclassification"""
  ]
  ParserVersion = "v1.0.0"


}
```