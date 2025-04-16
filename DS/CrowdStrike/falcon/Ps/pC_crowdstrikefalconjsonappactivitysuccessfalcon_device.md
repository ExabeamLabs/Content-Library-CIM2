#### Parser Content
```Java
{
Name = "crowdstrike-falcon-json-app-activity-success-falcon_device"
    Vendor = "CrowdStrike"
    Product = "Falcon"
    ExtractionType = json
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ"]
    ParserVersion = "v1.0.0"
    Conditions = [ """"falcon_device":""", """"ta_data":""" ]
    Fields = [
      """exa_json_path=$.falcon_device.device_id,exa_field_name=device_id"""
      """exa_json_path=$.falcon_device.cid,exa_field_name=cid"""
      """exa_json_path=$.falcon_device.external_ip,exa_field_name=dest_external_ip"""
      """exa_json_path=$.falcon_device.mac_address,exa_field_name=dest_mac"""
      """exa_json_path=$.falcon_device.hostname,exa_field_name=host"""
      """exa_json_path=$.falcon_device.last_login_user,exa_field_name=user"""
      """exa_json_path=$.falcon_device.last_login_uid,exa_field_name=user_uid"""
      """exa_json_path=$.falcon_device.last_login_user_sid,exa_field_name=user_sid"""
      """exa_json_path=$.falcon_device.policies,exa_field_name=policies"""
      """exa_json_path=$.falcon_device.system_product_name,exa_field_name=product_name"""
      """exa_json_path=$.falcon_device.os_version,exa_field_name=os_version"""
      """exa_json_path=$.falcon_device.os_build,exa_field_name=os_revision"""
      """exa_json_path=$.falcon_device.serial_number,exa_field_name=serial_num"""
      """exa_json_path=$.ta_data.Timestamp_value,exa_field_name=time"""
      """exa_json_path=$.falcon_device.system_manufacturer,exa_field_name=system_manufacturer"""
      """exa_json_path=$.falcon_device.platform_name,exa_field_name=system_type"""
      """exa_json_path=$.falcon_device.local_ip,exa_field_name=src_ip"""
    ]


}
```