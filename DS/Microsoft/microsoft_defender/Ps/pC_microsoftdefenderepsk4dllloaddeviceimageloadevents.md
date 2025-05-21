#### Parser Content
```Java
{
Name = "microsoft-defenderep-sk4-dll-load-deviceimageloadevents"
  Vendor = "Microsoft"
  Product = "Microsoft Defender"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  ExtractionType = json
  Conditions = [
    """"ActionType":"ImageLoaded"""",
    """DeviceImageLoadEvents"""",
    """"DeviceName":""""
  ]
  Fields = [
       """(time|TimeGenerated)"+:\s*"+({time}[^"]+)""""
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
       """"InitiatingProcessParentFileName"+:"((({parent_process_path}({parent_process_dir}[^"]+(\\|\/)+))?({parent_process_name}[^"]+)))""""
       """"InitiatingProcessIntegrityLevel"+:"+({process_integrity}[^"]+)"""
       """"InitiatingProcessParentId"+:({parent_process_id}\d+)"""
       """"InitiatingProcessCommandLine"+:"+"+({process_command_line}.+?)\s*"+,*"*(\w+"|$)"""
       """"InitiatingProcessId"+:({process_id}\d+)"""
       """"tenantId":"({tenant_id}[^",]+)"""
     """"FileName_s"+:\s*"+({object}[^"]+)"""
     """DeviceName"+:\s*"+({dest_host}[\w\-.]+)"""
     """exa_json_path=$.TimeGenerated,exa_field_name=time"""
     """exa_regex=(time|TimeGenerated)"+:\s*"+({time}[^"]+)""""
     """exa_json_path=$..ActionType,exa_field_name=action"""
     """exa_json_path=$.operationName,exa_field_name=operation"""
     """exa_json_path=$..DeviceName,exa_field_name=dest_host"""
     """exa_json_path=$..DeviceName,exa_field_name=host"""
     """exa_json_path=$.InitiatingProcessFileName,exa_field_name=process_name"""
     """exa_json_path=$.MD5,exa_field_name=hash_md5"""
     """exa_json_path=$..InitiatingProcessMD5,exa_field_name=hash_md5"""
     """exa_json_path=$.FileName,exa_regex=({file_path}({file_dir}[^"]+[\\\/]+)?({file_name}[^"\\\/\.]+?(\.({file_ext}\w+))?))"""
     """exa_json_path=$..FolderPath,exa_regex=({file_path}({file_dir}[^"]+[\\\/]+)?({file_name}[^"\\\/\.]+(\.({file_ext}\w+))?))"""
     """exa_json_path=$.FolderPath,exa_regex=({file_path}({file_dir}[^"]+[\\\/]+)?({file_name}[^"\\\/\.]+(\.({file_ext}\w+))?))"""
     """exa_json_path=$.InitiatingProcessParentId,exa_field_name=parent_process_id"""
     """exa_json_path=$.InitiatingProcessCommandLine,exa_field_name=process_command_line"""
     """exa_json_path=$..InitiatingProcessId,exa_field_name=process_id"""
     """exa_json_path=$..InitiatingProcessAccountSid,exa_field_name=user_sid"""
     """exa_json_path=$.tenantId,exa_field_name=tenant_id"""
     """exa_json_path=$.category,exa_field_name=category"""
     """exa_json_path=$..InitiatingProcessParentFileName,exa_field_name=parent_process_name"""
     """exa_json_path=$..InitiatingProcessFileName,exa_field_name=process_name"""
     """exa_json_path=$..InitiatingProcessParentId,exa_field_name=parent_process_id"""
     """exa_json_path=$..InitiatingProcessIntegrityLevel,exa_field_name=process_integrity"""
  ]
  ParserVersion = "v1.0.0"
  DupFields = ["category->event_name"]


}
```