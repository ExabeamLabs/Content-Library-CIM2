#### Parser Content
```Java
{
Name = microsoft-defenderep-cef-process-memory-allocate-advancedhunting
  ParserVersion = "v1.0.0"
  Conditions = ["""requestClientApplication=""", """AdvancedHunting-DeviceEvents""","""NtAllocateVirtualMemoryApiCall"""]

cef-defender-atp {
     Vendor = Microsoft
     TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
     Fields = [
       """time"+:\s*"+({time}[^"]+)"""",
       """operationName"+:\s*"+({operation}[^"]+)""",
       """category"+:\s*"+({category}[^"]+)""",
       """RemotePort"+:({dest_port}\d+)""",
       """RemoteIP"+:\s*"+({dest_ip}[^"]+)""",
       """protocol"+:\s*"+({protocol}[^"]+)""",
       """LocalIP"+:\s*"+({src_ip}[^"]+)""",
       """LocalPort"+:({src_port}\d+)""",
       """ActionType"+:\s*"+({action}[^"]+)""",
       """RemoteIPType"+:\s*"+(null|({direction}[^"]+))""",
       """DeviceName"+:\s*"+({dest_host}({host}[^"\.]+)?[^"]+)""",
       """InitiatingProcessAccountName"+:\s*"+(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|Système|system|local service|({user}[^"]+))""",
       """"ProcessIntegrityLevel"+:\s*"+({process_integrity}[^"]+)""",
       """InitiatingProcessAccountSid"+:\s*"+({user_sid}[^"]+)""",
       """InitiatingProcessFileName"+:\s*"+({process_name}[^"]+)""",
       """MD5"+:"+({hash_md5}[^"]+)""",
       """"FileName"+:\s*"+({file_name}[^"]+)""",
# azure_event_hub_namespace is removed
# azure_event_hub_name is removed
       """"FolderPath"+:\s*"+({file_path}({file_dir}[^"]*?[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?))"""",
       """"InitiatingProcessParentFileName"+:"+({parent_process}[^"]+)""",
       """"InitiatingProcessIntegrityLevel"+:"+({process_integrity}[^"]+)""",
       """"InitiatingProcessParentId"+:({parent_process_id}\d+)""",
       """"InitiatingProcessCommandLine"+:"+"+({process_command_line}.+?)\s*"+,*"*(\w+"|$)""",
       """"InitiatingProcessId"+:({process_id}\d+)""",
       """"tenantId":"({tenant_id}[^",]+)""",
     ]
     DupFields = ["category->event_name"
}
```