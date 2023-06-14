#### Parser Content
```Java
{
Name = microsoft-defenderep-json-link-create-success-shelllinkcreatefileevent
  ParserVersion = v1.0.0
  Product = Microsoft Defender for Endpoint
  Conditions = [ """"destinationServiceName":"Azure"""", """"category":"AdvancedHunting-DeviceEvents"""", """"ActionType":"ShellLinkCreateFileEvent"""" ]
  Fields = ${MicrosoftParserTemplates.json-defender-atp.Fields} [
    """"FileSizeInBytes\\*":({bytes}\d+)""",
    """hash_sha256":"({hash_sha256}[^"]+)""",
    """"ShellLinkShowCommand\\*":\\*"({additional_info}[^"]]+)"""
  ]

json-defender-atp {
   Vendor = "Microsoft"
   Product = "Microsoft Defender for Endpoint"
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
   Fields = [
     """time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d\d\d\d\dZ)"""",
     """operationName":\s*"({operation}[^"]+)""",
     """category":\s*"({category}[^"]+)""",
     """RemotePort":({dest_port}\d+)""",
     """RemoteIP":\s*"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
     """LocalIP":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """LocalPort":({src_port}\d+)""",
     """ActionType":\s*"({action}[^"]+)""",
     """DeviceName":\s*"({dest_host}({host}[^"\.]+)?[^"]+)""",
     """InitiatingProcessAccountName":\s*"(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|Système|system|local service|({user}[^"]+))""",
     """InitiatingProcessAccountSid":\s*"({user_sid}[^"]+)""",
     """"InitiatingProcessFolderPath":\s*"({process_path}({process_dir}[^"]*?)\\+({process_name}[^"\\\/]+))""""
     """InitiatingProcessFileName":\s*"({process_name}[^"]+)"""",
     """MD5":"({hash_md5}[^"]+)""",
     """"FileName":\s*"({file_name}[^"]+)""",
     """"FolderPath":\s*"({file_path}({file_dir}[^"]*?[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?))"""",
     """"InitiatingProcessParentFileName":"({parent_process}[^"]+)""",
     """"InitiatingProcessParentId":({parent_process_id}\d+)""",
     """"InitiatingProcessCommandLine":""({process_command_line}.+?)\s*",*"*(\w+"|$)""",
     """"InitiatingProcessId":({process_id}\d+)""",
     """"tenantId":"({tenant_id}[^",]+)""",
     """"InitiatingProcessAccountDomain":\s*"({domain}[^"]+)""",
     """AccountUpn":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""",
     """SHA1":"({hash_sha1}[^"]+)"""",
   ]
   DupFields = ["category->event_name"
}
```