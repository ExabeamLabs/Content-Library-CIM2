#### Parser Content
```Java
{
Name = "crowdstrike-falcon-mix-peripheral-storage-insert-success-removablemediavolumemounted"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch_sec"
ExtractionType = json
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
      """exa_json_path=$.aip,exa_field_name=host"""
      """exa_json_path=$.timestamp,exa_field_name=time"""
      """exa_json_path=$.event_simpleName,exa_field_name=event_code"""
      """exa_json_path=$.aid,exa_field_name=aid"""
      """exa_json_path=$.VolumeRealDeviceName,exa_field_name=device_type"""
      """exa_json_path=$.VolumeMountPoint,exa_field_name=device_id"""
      """exa_regex=suser=(system|({user}[\w\.\-]{1,40}\$?))"""
      """exa_json_path=$.DiskParentDeviceInstanceId,exa_field_name=vendor_id"""
      """exa_json_path=$.cid,exa_field_name=cid"""
      """exa_json_path=$.event_platform,exa_field_name=os"""
]
DupFields = [
"process_id->process_name"
"device_type->volume_name"
"event_code->operation"
]
ParserVersion = "v1.0.0"


}
```