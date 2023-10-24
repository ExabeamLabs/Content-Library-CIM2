#### Parser Content
```Java
{
Name = "code42-incydr-json-peripheral-storage-activity-success-deviceaddress"
Vendor = "Code42"
Product = "Code42 Incydr"
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
""""deviceAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""deviceAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""deviceRemoteAddress":\s*"({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
""""deviceRemoteAddress":\s*"({src_translated_ip}\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4})"""
""""timestamp":\s*({time}\d\d\d\d\d\d\d\d\d\d)"""
""""userUid":\s"({user_uid}[^"]+)"""
""""eventType":\s"({operation}[^"]+)"""
""""busType":\s"({device_type}[^"]+)"""
""""deviceGuid":\s"({device_id}[^"]+)"""
""""deviceName":\s"({device_name}[^"]+)"""
""""mediaName":\s"({device_name}[^"]+)"""
""""serialNumber":\s"(unknown|({usb_serial_number}[^"]+))"""
""""mediaName"":\s"({device_name}[^"]+)"""
""""vendorName":\s"({vendor_name}[^"]+)"""
""""vendorName":\s"({usb_vendor}[^"]+)"""
""""volumeName":\s"(unknown|[^\(]*?({drive_letter}[^"]+))"""
]
ParserVersion = "v1.0.0"


}
```