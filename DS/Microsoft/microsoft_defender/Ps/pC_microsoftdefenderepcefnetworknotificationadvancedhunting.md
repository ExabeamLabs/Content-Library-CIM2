#### Parser Content
```Java
{
Name = microsoft-defenderep-cef-network-notification-advancedhunting
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft Defender
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = ["""destinationServiceName =Azure""", """"category":"AdvancedHunting-DeviceNetworkInfo""""]
  Fields = ${DLMicrosoftParsersTemplates.cef-defender-atp.Fields} [
     """time"+:\s*"+({time}[^"]+)"""",
     """operationName"+:\s*"+({operation}[^"]+)""",
     """category"+:\s*"+({category}[^"]+)""",
     """DeviceName"+:\s*"+({dest_host}({host}[\w\-.]+))""",
     """category"+:"+({event_name}[^"]+)""",
     """DeviceId":"({device_id}[^"]+)"""",
     """IPAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
     """MacAddress":"({src_mac}[^"]+)"""",
# subnet_mask is removed
  ]

cef-defender-atp {
     Vendor = Microsoft
     TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
     Fields = [
       """time"+:\s*"+({time}[^"]+)"""",
       """operationName"+:\s*"+({operation}[^"]+)""",
       """category"+:\s*"+({category}[^"]+)""",
       """RemotePort"+:({dest_port}\d+)""",
       """RemoteIP"+:\s*"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
       """protocol"+:\s*"+({protocol}[^"]+)""",
       """LocalIP"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
       """LocalPort"+:({src_port}\d+)""",
       """ActionType"+:\s*"+({result}[^"]+)""",
       """DeviceName"+:\s*"+({dest_host}({host}[\w\-.]+))""",
       """InitiatingProcessAccountName"+:\s*"+(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|Système|system|local service|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
       """"ProcessIntegrityLevel"+:\s*"+({process_integrity}[^"]+)""",
       """InitiatingProcessAccountSid"+:\s*"+({user_sid}[^"]+)""",
       """"InitiatingProcessFolderPath":\s*"({process_path}({process_dir}[^"]+)[\\\/]({process_name}[^"]+))""",
       """InitiatingProcessFileName"+:\s*"+({process_name}[\w\.]+)"""",
       """MD5"+:"+({hash_md5}[^"]+)""",
       """"FileName"+:\s*"+({file_name}[^"]+)""",
# azure_event_hub_namespace is removed
# azure_event_hub_name is removed
       """"FolderPath"+:\s*"+({file_path}({file_dir}[^"]*?[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?))"""",
       """"InitiatingProcessParentFileName"+:"((({parent_process_path}({parent_process_dir}[^"]+(\\|\/)+))?({parent_process_name}[^"]+)))""",
       """"InitiatingProcessIntegrityLevel"+:"+({process_integrity}[^"]+)""",
       """"InitiatingProcessParentId"+:({parent_process_id}\d+)""",
       """"InitiatingProcessCommandLine"+:"+"+({process_command_line}.+?)\s*"+,*"*(\w+"|$)""",
       """"InitiatingProcessId"+:({process_id}\d+)""",
       """"tenantId":"({tenant_id}[^",]+)""",
       """"SHA1":"({hash_sha1}[^"]+)"""",
       """"InitiatingProcessSHA1":"({hash_sha1}[^"]+)""""
     ]
     DupFields = ["category->event_name"
}
```