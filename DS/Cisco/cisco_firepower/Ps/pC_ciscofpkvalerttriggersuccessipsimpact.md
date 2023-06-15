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
      """\simpactAlertData.sourceAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """\simpactAlertData.destinationAddress=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """\s\[Priority: ({alert_severity}\d+)\]""",
      """\simpactAlertData.description=\[[^\]]+\] "({alert_name}[^"]+)""",
      """\s\[Classification: ({alert_type}[^\]]+)\]"""
  ]
  ParserVersion = "v1.0.0"


}
```