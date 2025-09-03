#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-peripheral-storage-activity-dcusb
  ParserVersion = "v1.0.0"
  Conditions = [ """"event_simpleName":"DcUsb""" ]
  Fields = ${CrowdStrikeParsersTemplates.cef-crowdstrike-app-activity-temp-aa.Fields} [
  """"id":"({alert_id}[\w-]+?)""""
  """"event_simpleName":"({operation_details}[^"]+)"""
  """"DeviceInstanceId":"({device_id}[^"]+)"""
  """"DevicePropertyDeviceDescription":"({device_description}[^"]+?)\s*""""
  """"event_platform":"({os}[^"]+)""""
  """"cid":"({cid}[^"]+)"""
  ]


}
```