#### Parser Content
```Java
{
Name = microsoft-defenderep-sk4-registry-modify-advancedhunting
    ParserVersion = v1.0.0
    Vendor = Microsoft
    Product = Microsoft Defender
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
    ExtractionType = json
    Conditions = ["""DeviceRegistryEvents""""]
    Fields = [
       """"(time|TimeGenerated)"+:\s*"+({time}[^"]+)"""",
       """category"+:\s*"+({operation}[^"]+)""",
       """ActionType"+:\s*"+({operation_type}[^"]+)""",
       """DeviceName"+:\s*"+({dest_host}({host}[\w\-.]+))""",
       """InitiatingProcessAccountName"+:\s*"+(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|Système|system|local service|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
       """InitiatingProcessAccountSid"+:\s*"+({user_sid}[^"]+)""",
       """InitiatingProcessFileName"+:\s*"+({process_name}[^"]+)""",
       """"InitiatingProcessFolderPath"+:\s*"+({file_path}({file_dir}[^"]*?[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?))"""",
       """"InitiatingProcessParentFileName"+:"+({parent_process_name}[^"]+)""",
       """"InitiatingProcessCommandLine"+:"+"+({process_command_line}.+?)\s*"+,*"*(\w+"|$)""",
       """"InitiatingProcessId"+:({process_id}\d+)""",
       """operationName":\s*"({action}[^"]+)""",
       """"RegistryKey":"({registry_path}({registry_key}[^"]+))"""",
       """"RegistryValueName":"({registry_value}[^"]+)"""",
       """"RegistryValueData":"({registry_details}[^"]+)""""
       """exa_json_path=$.time,exa_field_name=time"""
       """exa_regex="(time|TimeGenerated)"+:\s*"+({time}[^"]+)"""",
       """exa_json_path=$.category,exa_field_name=operation"""
       """exa_json_path=$..ActionType,exa_field_name=operation_type"""
       """exa_json_path=$..DeviceName,exa_field_name=host"""
       """exa_json_path=$..DeviceName,exa_field_name=dest_host"""
       """exa_json_path=$..InitiatingProcessAccountName,exa_field_name=operation_type"""
       """exa_json_path=$..InitiatingProcessAccountSid,exa_field_name=user_sid"""
       """exa_regex="InitiatingProcessFolderPath"+:\s*"+({file_path}({file_dir}[^"]*?[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?))"""",
       """exa_json_path=$..InitiatingProcessParentFileName,exa_field_name=parent_process_name"""
       """exa_json_path=$..InitiatingProcessCommandLine,exa_field_name=process_command_line"""
       """exa_json_path=$..InitiatingProcessId,exa_field_name=process_id"""
       """exa_json_path=$.operationName,exa_field_name=action"""
       """exa_json_path=$..RegistryKey,exa_regex=({registry_path}({registry_key}[^"]+))"""
       """exa_json_path=$..RegistryValueName,exa_field_name=registry_value"""
       """exa_json_path=$..RegistryValueData,exa_field_name=registry_details"""
    ]
    DupFields = ["operation_type->event_name", "file_path->process_path", "file_dir->process_dir"]


}
```