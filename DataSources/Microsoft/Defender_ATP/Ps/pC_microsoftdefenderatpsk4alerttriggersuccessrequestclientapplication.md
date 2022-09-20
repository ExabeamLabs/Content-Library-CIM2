#### Parser Content
```Java
{
Name = microsoft-defenderatp-sk4-alert-trigger-success-requestclientapplication
  Product = Defender ATP
  ParserVersion = v1.0.0
  Conditions = [""""Category":""", """requestClientApplication=""", """AdvancedHunting-DeviceAlertEvents"""]
  Fields = ${MicrosoftParserTemplates.cef-defender-atp.Fields} [
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