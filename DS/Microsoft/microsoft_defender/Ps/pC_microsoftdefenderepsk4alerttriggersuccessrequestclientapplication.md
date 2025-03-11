#### Parser Content
```Java
{
Name = microsoft-defenderep-sk4-alert-trigger-success-requestclientapplication
  Product = Microsoft Defender
  ParserVersion = v1.0.0
  Conditions = [""""Category":""", """requestClientApplication=""", """AdvancedHunting-DeviceAlertEvents"""]
  Fields = ${MicrosoftParserTemplates.cef-defender-atp-3.Fields} [
     """Category":\s*"({alert_name}[^"]+)""",
     """Title":\s*"({additional_info}[^"]+)""",
     """FileName":\s*"({process_name}[^"]+)""",
     """Severity":\s*"({alert_severity}[^"]+)""",
     """AlertId":\s*"({alert_id}[^"]+)"""
     """DeviceName":\s*"({src_host}[^"]+)""",
     """RemoteUrl":\s*"({malware_url}[^"]+)""",
     """MD5":"({hash_md5}[^"]+)"""
  ]
  DupFields = [ "category->alert_type" ]

cef-defender-atp-3 {
   Vendor = "Microsoft"
   Product = "Microsoft Defender"
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
   Fields = [
     """time"+:\s*"+({time}[^"]+)"""",
     """operationName"+:\s*"+({operation}[^"]+)""",
     """category"+:\s*"+({category}[^"]+)""",
     """RemotePort"+:({dest_port}\d+)""",
     """RemoteIP"+:\s*"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
     """protocol"+:\s*"+({protocol}[^"]+)""",
     """LocalIP"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """LocalPort"+:({src_port}\d+)""",
     """ActionType"+:\s*"+({action}[^"]+)""",
     """RemoteIPType"+:\s*"+(null|({direction}[^"]+))""",
     """DeviceName"+:\s*"+({dest_host}({host}[\w\-.]+))""",
     """InitiatingProcessAccountName"+:\s*"+(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|Système|system|local service|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""",
     """"ProcessIntegrityLevel"+:\s*"+({process_integrity}[^"]+)""",
     """InitiatingProcessAccountSid"+:\s*"+({user_sid}[^"]+)""",
     """"InitiatingProcessFolderPath":\s*"({process_path}({process_dir}[^"]*?)\\+({process_name}[^"\\\/]+))""""
     """InitiatingProcessFileName"+:\s*"+({process_name}[\w\.\-]+)"""",
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
     """"InitiatingProcessSHA1":"({hash_sha1}[^"]+)"""",
   ]
   DupFields = ["category->event_name"
}
```