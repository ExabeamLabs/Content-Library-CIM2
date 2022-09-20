#### Parser Content
```Java
{
Name = cisco-fp-kv-alert-trigger-success-ipsimpact
  Vendor = Cisco
  Product = Cisco Firepower
  TimeFormat = "dd MMMM yyyy HH:mm:ss"
  Conditions = [ """DeviceType=Estreamer""", """recordType=IPS_IMPACT_ALERT""" ]
  Fields = [
      """\stimestamp=({time}\d\d \w{3} \d{4} \d\d:\d\d:\d\d)""",
      """\sDeviceAddress=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """\simpactAlertData.sourceAddress=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """\simpactAlertData.destinationAddress=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """\s\[Priority: ({alert_severity}\d+)\]""",
      """\simpactAlertData.description=\[[^\]]+\] "({alert_name}[^"]+)""",
      """\s\[Classification: ({alert_type}[^\]]+)\]"""
  ]
  ParserVersion = "v1.0.0"


}
```