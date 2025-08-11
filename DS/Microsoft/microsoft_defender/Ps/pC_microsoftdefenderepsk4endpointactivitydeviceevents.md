#### Parser Content
```Java
{
Name = "microsoft-defenderep-sk4-endpoint-activity-deviceevents"
  Conditions = [
    """requestClientApplication="""
    """AdvancedHunting-DeviceEvents"""
  ]
  Fields = ${MicrosoftParserTemplates.cef-defender-atp-1.Fields} [
     """ActionType"+:\s*"+({event_name}[^"]+)"""
     """operationName"+:\s*"+({action}[^"]+)"""
     """DeviceName"+:\s*"+({dest_host}[\w\-.]+)"""
     """"FileName"+:\s*"+({file_name}[^"]+)"""
     """"MD5"+:"+({hash_md5}[^"]+)"""
  ]
  ParserVersion = "v1.0.0"

cef-defender-atp-1 = {
     Vendor = "Microsoft"
     Product = "Microsoft Defender"
     TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
     Fields = [
       """time"+:\s*"+({time}[^"]+)""""
       """operationName"+:\s*"+({operation}[^"]+)"""
       """category"+:\s*"+({category}[^"]+)"""
       """RemotePort"+:({dest_port}\d+)"""
       """RemoteIP"+:\s*"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
       """protocol"+:\s*"+({protocol}[^"]+)"""
       """LocalIP"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
       """LocalPort"+:({src_port}\d+)"""
       """ActionType"+:\s*"+({action}[^"]+)"""
       """RemoteIPType"+:\s*"+(null|({direction}[^"]+))"""
       """DeviceName"+:\s*"+({dest_host}({host}[\w\-.]+))"""
       """InitiatingProcessAccountName"+:\s*"+(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|Système|system|local service|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
       """"ProcessIntegrityLevel"+:\s*"+({process_integrity}[^"]+)"""
       """InitiatingProcessAccountSid"+:\s*"+({user_sid}[^"]+)"""
       """InitiatingProcessFileName"+:\s*"+({process_name}[^"]+)"""
       """MD5"+:"+({hash_md5}[^"]+)"""
       """"FileName"+:\s*"+({file_name}[^"]+)"""
# azure_event_hub_namespace is removed
# azure_event_hub_name is removed
       """"FolderPath"+:\s*"+({file_path}({file_dir}[^"]*?[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?))""""
       """"InitiatingProcessParentFileName"+:"+({parent_process_name}[^"]+)"""
       """"InitiatingProcessIntegrityLevel"+:"+({process_integrity}[^"]+)"""
       """"InitiatingProcessParentId"+:({parent_process_id}\d+)"""
       """"InitiatingProcessCommandLine"+:"+"+({process_command_line}.+?)\s*"+,*"*(\w+"|$)"""
       """"InitiatingProcessId"+:({process_id}\d+)"""
       """"tenantId":"({tenant_id}[^",]+)"""
     ]
     DupFields = ["category->event_name"]
   }

cef-defender-atp-3 {
   Vendor = "Microsoft"
   Product = "Microsoft Defender"
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
     """ActionType"+:\s*"+({action}[^"]+)""",
     """RemoteIPType"+:\s*"+(null|({direction}[^"]+))""",
     """DeviceName"+:\s*"+({dest_host}({host}[\w\-.]+))""",
     """InitiatingProcessAccountName"+:\s*"+(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|Système|system|local service|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""",
     """"ProcessIntegrityLevel"+:\s*"+({process_integrity}[^"]+)""",
     """InitiatingProcessAccountSid"+:\s*"+({user_sid}[^"]+)""",
     """InitiatingProcessFileName"+:\s*"+({process_name}[\w\.\-]+)"""",
     """"InitiatingProcessFolderPath":\s*"(({process_path}({process_dir}[^"]+?[\\\/]+)({process_name}[^"\\\/]+(\.[a-zA-Z]+)))|({=process_dir}[^"]+))""""
     """MD5"+:"+({hash_md5}[^"]+)""",
     """"FileName"+:\s*"+({file_name}[^"]+)""",
# azure_event_hub_namespace is removed
# azure_event_hub_name is removed
     """"FolderPath"+:\s*"+({file_path}({file_dir}[^"]*?[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?))"""",
     """"InitiatingProcessParentFileName":"({parent_process_path}({parent_process_dir}[^"]+?[\\\/]+)?({parent_process_name}[^"\\\/]+))"""",
     """"InitiatingProcessIntegrityLevel"+:"+({process_integrity}[^"]+)""",
     """"InitiatingProcessParentId"+:({parent_process_id}\d+)""",
     """"InitiatingProcessCommandLine"+:"+"+({process_command_line}.+?)\s*"+,*"*(\w+"|$)""",
     """"InitiatingProcessId"+:({process_id}\d+)""",
     """"tenantId":"({tenant_id}[^",]+)""",
     """"SHA1":"({hash_sha1}[^"]+)"""",
     """"InitiatingProcessSHA1":"({hash_sha1}[^"]+)"""",
   ]
   DupFields = ["category->event_name"
}
```