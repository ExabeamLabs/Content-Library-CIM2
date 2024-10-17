#### Parser Content
```Java
{
Name = symantec-edr-json-app-notification-success-detectedonstream
  ExtractionType = json
  ParserVersion = "v1.0.0"
  Conditions = [ """A read lag is detected on stream""","""\"event_id\":21001""","""Symantec""" ]
  Fields = ${DLSymantecParserTemplates.symantec-system-info-template.Fields}[
    """({event_name}A read lag is detected on stream)""",
  ]

symantec-system-info-template = {
    Vendor = Symantec
    Product = Symantec Advanced Threat Protection
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
    Fields = [
      """(\\)?"time(\\)?":(\\)?"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """\\"message\\":\\"({additional_info}.+?)\\",\\"\w+\\":""",
      """(\\)?"user_name(\\)?":(\\)?"(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^"\\=]+))(\\)?"""",
      """(\\)?"event_id(\\)?":({event_code}\d+)""",
      """(\\)?"user_uid(\\)?":(\\)?"({user_uid}[^\\"]+)""",
      """(\\)?"destinationServiceName(\\)?":(\\)?"({app}[^\\"]+)""",
      """(\\)?"session_uid(\\)?":(\\)?"({session_id}[^\\"]+)""",
      """(\\)?"ipv4(\\)?":(\\)?"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """(\\)?"device_os_name(\\)?":(\\)?"({os}[^"\\]+)""",
      """(\\)?"device_name(\\)?":(\\)?"({host}[\w\-.]+)""",
      """(\\)?"device_domain(\\)?":(\\)?"({domain}[^"\\]+)"""
      """exa_json_path=$.time,exa_field_name=time"""
      """exa_regex=(\\)?"time(\\)?":(\\)?"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """exa_json_path=$.message,exa_field_name=additional_info"""
      """exa_json_path=$.destinationServiceName,exa_field_name=app"""
      """exa_regex="ipv4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """exa_json_path=$.device_os_name,exa_field_name=os"""
      """exa_json_path=$.device_name,exa_field_name=host"""
      """exa_regex="user_name":"(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^"=]+))"""",
      """exa_regex="device_name":"({host}[\w\-.]+)""",
      """exa_regex="device_domain":"({domain}[^"\\]+)"""
      """exa_regex="device_os_name":"({os}[^"\\]+)""",
      """exa_json_path=$.user_uid,exa_field_name=user_uid"""
      """exa_regex="time(\\)?":(\\)?"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """exa_regex=\\"message\\":\\"({additional_info}.+?)\\",\\"\w+\\":""",
      """exa_regex=(\\)?"user_name(\\)?":(\\)?"(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^"\\=]+))(\\)?"""",
      """exa_regex=(\\)?"event_id(\\)?":({event_code}\d+)""",
      """exa_regex=(\\)?"user_uid(\\)?":(\\)?"({user_uid}[^\\"]+)""",
      """exa_regex=(\\)?"destinationServiceName(\\)?":(\\)?"({app}[^\\"]+)""",
      """exa_regex=(\\)?"session_uid(\\)?":(\\)?"({session_id}[^\\"]+)""",
      """exa_regex=(\\)?"ipv4(\\)?":(\\)?"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """exa_regex=(\\)?"device_os_name(\\)?":(\\)?"({os}[^"\\]+)""",
      """exa_regex=(\\)?"device_name(\\)?":(\\)?"({host}[\w\-.]+)""",
      """exa_regex=(\\)?"device_domain(\\)?":(\\)?"({domain}[^"\\]+)"""
    
}
```