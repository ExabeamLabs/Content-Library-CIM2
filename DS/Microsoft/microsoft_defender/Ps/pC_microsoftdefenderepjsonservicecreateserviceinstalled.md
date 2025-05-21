#### Parser Content
```Java
{
Name = "microsoft-defenderep-json-service-create-serviceinstalled"
  Conditions = [  """DeviceEvents"""", """"ActionType":"ServiceInstalled"""" ]
  ParserVersion = "v1.0.0"
  Fields = ${MicrosoftParserTemplates.json-defender-atp.Fields} [
      """exa_json_path=$..AdditionalFields,exa_regex=ServiceName\\":\\"({service_name}[^,]+)\\",""",
      """AdditionalFields":[^\}]*?ServiceName\\+?":\\+?"({service_name}[^,]+)\\+?","""
	]

json-defender-atp {
   Vendor = "Microsoft"
   Product = "Microsoft Defender"
   TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd HH:mm:ss.SSSSSSSZ"]
   Fields = [
     """time":\s*"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d(.\d{1,7})?Z)"""",
     """(time|TimeGenerated)":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d\d\d\d\dZ)"""",
     """operationName":\s*"({operation}[^"]+)""",
     """category":\s*"({category}[^"]+)""",
     """RemotePort":\s*({dest_port}\d+)""",
     """RemoteIP":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
     """LocalIP":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """LocalPort":\s*({src_port}\d+)""",
     """ActionType":\s*"({action}[^"]+)""",
     """"DeviceId":"({device_id}[^"]+)"""",
     """DeviceName":\s*"({dest_host}({host}[\w\-.]+))""",
     """InitiatingProcessAccountName":\s*"(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|Système|system|local service|({user}[\w\.\-\!\#\^\~]{1,40}\$?)"|({full_name}[^"]+))""",
     """InitiatingProcessAccountSid":\s*"({user_sid}[^"]+)""",
     """"InitiatingProcessFolderPath":\s*"({process_path}({process_dir}[^"]*?)\\+({process_name}[^"\\\/]+))""""
     """InitiatingProcessFileName":\s*"({process_name}[^"]+)"""",
     """MD5":\s*"({hash_md5}[^"]+)""",
     """"FileName":\s*"({file_name}[^"]+)""",
     """"FolderPath":\s*"({file_path}({file_dir}[^"]*?[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?))"""",
     """"InitiatingProcessParentFileName":\s*"((({parent_process_path}({parent_process_dir}[^"]+(\\|\/)+))?({parent_process_name}[^"]+)))""",
     """"InitiatingProcessParentId":\s*({parent_process_id}\d+)""",
     """"InitiatingProcessCommandLine":\s*"({process_command_line}.+?)\s*",*"*(\w+"|$)""",
     """"InitiatingProcessId":\s*({process_id}\d+)""",
     """"tenantId":\s*"({tenant_id}[^",]+)""",
     """"InitiatingProcessAccountDomain":\s*"({domain}[^"]+)""",
     """AccountUpn":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""",
     """SHA1":\s*"({hash_sha1}[^"]+)"""",
     """"InitiatingProcessVersionInfoInternalFileName":\s*"({service_name}[^"]+)""",
     """Description":\s*"({additional_info}[^"]+)"""",
     """"InitiatingProcessSHA256":\s*"({hash_sha256}[^",]+)"""",
     """"InitiatingProcessSHA1":\s*"({hash_sha1}[^"]+)"""",
     """"DeviceType":"({device_class}[^"]+)""""
     """"OSPlatform":"({os}[^"]+)""""
     """exa_json_path=$.time,exa_field_name=time"""
     """exa_json_path=$.TimeGenerated,exa_field_name=time"""
     """exa_json_path=$.operationName,exa_field_name=operation"""
     """exa_json_path=$.category,exa_field_name=category"""
     """exa_json_path=$.ActionType,exa_field_name=action"""
     """exa_json_path=$..RemotePort,exa_field_name=dest_port"""
     """exa_json_path=$..RemoteIP,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
     """exa_json_path=$..LocalIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
     """exa_json_path=$..LocalPort,exa_field_name=src_port"""
     """exa_json_path=$..ActionType,exa_field_name=action"""
     """exa_json_path=$..DeviceName,exa_field_name=dest_host"""
     """exa_json_path=$..DeviceName,exa_field_name=host"""
     """exa_json_path=$..InitiatingProcessAccountName,exa_regex=(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|Système|system|local service|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^",]+))"""
     """exa_json_path=$..InitiatingProcessAccountSid,exa_field_name=user_sid"""
     """exa_json_path=$..InitiatingProcessFolderPath,exa_regex=({process_path}({process_dir}[^"]+)\\+({process_name}[^"\\\/]+))"""
     """exa_json_path=$..InitiatingProcessParentId,exa_field_name=parent_process_id"""
     """exa_json_path=$..InitiatingProcessCommandLine,exa_field_name=process_command_line"""
     """exa_json_path=$..InitiatingProcessId,exa_field_name=process_id"""
     """exa_json_path=$..InitiatingProcessFileName,exa_field_name=process_name"""
     """exa_json_path=$..InitiatingProcessMD5,exa_field_name=hash_md5"""
     """exa_json_path=$..FileName,exa_field_name=file_name"""
     """exa_regex="FolderPath":\s*"({file_path}({file_dir}[^"]+[\\\/]+)?({file_name}[^"]+?(\.({file_ext}\w+))?))""""
     """exa_regex="InitiatingProcessParentFileName":\s*"((({parent_process_path}({parent_process_dir}[^"]+(\\|\/)+))?({parent_process_name}[^"]+)))""""
     """exa_json_path=$.tenantId,exa_field_name=tenant_id"""
     """exa_json_path=$..InitiatingProcessAccountDomain,exa_field_name=domain"""
     """exa_json_path=$..InitiatingProcessAccountUpn,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
     """exa_json_path=$..InitiatingProcessSHA1,exa_field_name=hash_sha1"""
     """exa_json_path=$..InitiatingProcessVersionInfoInternalFileName,exa_field_name=service_name"""
     """exa_json_path=$..InitiatingProcessVersionInfoFileDescription,exa_field_name=additional_info"""
     """exa_json_path=$..InitiatingProcessSHA256,exa_field_name=hash_sha256"""
     """exa_json_path=$..InitiatingProcessSHA1,exa_field_name=hash_sha1"""
     """exa_json_path=$..SHA1,exa_field_name=hash_sha1"""
     """exa_json_path=$..DeviceType,exa_field_name=device_type"""
     """exa_json_path=$..OSPlatform,exa_field_name=os"""
     """exa_json_path=$..AdditionalFields,exa_regex=DeviceId\\":\\"({device_id}[^,]+)\\","""
     """exa_json_path=$..AdditionalFields,exa_regex=DeviceDescription\\":\\"\\*({device_description}[^,]+)\\","""
     """AdditionalFields":.*DeviceId\\":\\"({device_id}[^,]+)\\","""
     """AdditionalFields":.*DeviceDescription\\":\\"\\*({device_description}[^,]+)\\","""
   ]
   DupFields = ["category->event_name"
}
```