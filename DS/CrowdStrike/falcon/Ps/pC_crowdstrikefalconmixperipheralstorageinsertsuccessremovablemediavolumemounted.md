#### Parser Content
```Java
{
Name = "crowdstrike-falcon-mix-peripheral-storage-insert-success-removablemediavolumemounted"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch_sec"
Conditions = [
""""event_simpleName":"RemovableMediaVolumeMounted""""
]
Fields = [
      """"+aip"+:"+({host}[^"]+)"+,"""
      """"timestamp":"({time}\d{10})""",
      """"event_simpleName":"({event_code}[^"]+)""",
      """"aid":"({aid}[^"]+)""",
      """"VolumeRealDeviceName":"({device_type}[^"]+)""",
      """VolumeMountPoint":"\\\\\?\?\\\\Volume\{({device_id}[^}]+)""",
      """suser=(system|({user}[\w\.\-]{1,40}\$?))""",
      """DiskParentDeviceInstanceId"+:"+USB\\+VID_({vendor_id}[^&]+)&PID_({process_id}[^\\&]+).*?\\+({device_id}[^"]+)""",
      """"cid":"({cid}[^"]+)"""
      """"event_platform":"({os}[^"]+)""""
]
DupFields = [
"process_id->process_name"
"device_type->volume_name"
"event_code->operation"
]
ParserVersion = "v1.0.0"


}
```