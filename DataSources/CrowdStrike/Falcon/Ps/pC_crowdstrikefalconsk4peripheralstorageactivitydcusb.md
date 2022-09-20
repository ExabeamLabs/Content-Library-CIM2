#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-peripheral-storage-activity-dcusb
  ParserVersion = "v1.0.0"
  Conditions = [ """"event_simpleName":"DcUsb""" ]
  Fields = ${DLCrowdStrikeParserTemplates.cef-crowdstrike-app-activity-temp-dl.Fields} [
  """"id":"({alert_id}[\w-]+?)""""
  """"event_simpleName":"({activity_details}[^"]+)"""
  """"DeviceInstanceId":"({device_id}[^"]+)"""
  """"DevicePropertyDeviceDescription":"({device_type}[^"]+?)\s*""""
  """"event_platform":"({os}[^"]+)""""
  ]

cef-crowdstrike-app-activity-temp-dl = {
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch_sec"
  Fields = [
    """"timestamp":\s*"*({time}\d{10})""",
    """"UserIp":\s*"({src_ip}[^"]+)""",
    """\WdestinationServiceName =({app}.+?)\s+\w+="""
    """"event_simpleName":\s*"({event_code}[^"]+)""",
    """"aid":\s*"({aid}[^"]+)""",
    """"(ImageFileName|TargetFileName)":\s*"({file_path}[^"]+)""",
    """"(ImageFileName|TargetFileName)":\s*"({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+\.({file_ext}[^\\\/"]+))"""
    """"UserName":\s*"({user}[^"]+?)""""
    """"aip":\s*"({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""""
    """"name":\s*"({alert_type}[^"]+)"""
    """"ClientComputerName":\s*"({src_host}[^"]+)"""
  
}
```