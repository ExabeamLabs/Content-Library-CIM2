#### Parser Content
```Java
{
Name = "code42-incydr-json-peripheral-storage-activity-success-deviceaddress"
Vendor = "Code42"
Product = "Code42 Incydr"
ExtractionType = json
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""formattedTimestamp"""
"""deviceAddress"""
"""deviceRemoteAddress"""
"""operatingSystemUser"""
""""modular_input_consumption_time":"""
"""DEVICE_DISAPPEARED"""
]
Fields = [
"""exa_json_path=$.deviceAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""exa_json_path=$.deviceRemoteAddress,exa_regex=({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
"""exa_json_path=$.deviceRemoteAddress,exa_regex=({src_translated_ip}\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4})"""
"""exa_json_path=$.timestamp,exa_field_name=time"""
"""exa_json_path=$.userUid,exa_field_name=user_uid"""
"""exa_json_path=$.eventType,exa_field_name=operation"""
"""exa_json_path=$.detectionDevice.busType,exa_field_name=device_class"""
"""exa_json_path=$.deviceGuid,exa_field_name=device_id"""
"""exa_json_path=$.detectionDevice.deviceName,exa_field_name=device_description"""
"""exa_json_path=$.detectionDevice.mediaName,exa_field_name=device_description"""
"""exa_json_path=$.detectionDevice.serialNumber,exa_field_name=usb_serial_number,exa_match_expr=!InList(($.detectionDevice.serialNumber), "unknown")""",
"""exa_json_path=$.detectionDevice.vendorName,exa_field_name=vendor_name"""
"""exa_json_path=$.detectionDevice.volumes[0].volumeName,exa_field_name=drive_letter"""
]
DupFields = [ "vendor_name->usb_vendor" ]
ParserVersion = "v1.0.0"


}
```