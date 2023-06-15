#### Parser Content
```Java
{
Name = microsoft-defenderep-sk4-registry-modify-advancedhunting
    ParserVersion = v1.0.0
    Vendor = Microsoft
    Product = Microsoft Defender for Endpoint
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
    Conditions = [""""category":"AdvancedHunting-DeviceRegistryEvents""""]
    Fields = [
       """time"+:\s*"+({time}[^"]+)"""",
       """category"+:\s*"+({operation}[^"]+)""",
       """ActionType"+:\s*"+({operation_type}[^"]+)""",
       """DeviceName"+:\s*"+({dest_host}({host}[^"\.]+)?[^"]+)""",
       """InitiatingProcessAccountName"+:\s*"+(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|Système|system|local service|({user}[^"]+))""",
       """InitiatingProcessAccountSid"+:\s*"+({user_sid}[^"]+)""",
       """InitiatingProcessFileName"+:\s*"+({process_name}[^"]+)""",
       """"InitiatingProcessFolderPath"+:\s*"+({file_path}({file_dir}[^"]*?[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?))"""",
       """"InitiatingProcessParentFileName"+:"+({parent_process}[^"]+)""",
       """"InitiatingProcessCommandLine"+:"+"+({process_command_line}.+?)\s*"+,*"*(\w+"|$)""",
       """"InitiatingProcessId"+:({process_id}\d+)""",
       """operationName":\s*"({action}[^"]+)""",
       """"RegistryKey":"({registry_path}({registry_key}[^"]+))"""",
       """"RegistryValueName":"({registry_value}[^"]+)"""",
       """"RegistryValueData":"({registry_details}[^"]+)""""
    ]
    DupFields = ["operation_type->event_name", "file_path->process_path", "file_dir->process_dir"]


}
```