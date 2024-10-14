#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-privilege-use-success-4674-1"
ExtractionType = json
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """An operation was attempted on a privileged object."""
  """"event_id":4674""" 
]
Fields = [
  """({event_name}An operation was attempted on a privileged object)"""
  """\"@timestamp\"\s*:\s*\"({time}.+?)\""""
  """\"hostname\":\"({host}[\w\-.]*)"""
  """\"host\":\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """({event_code}4674)"""
  """\"keywords\":\[\"({result}.+?)\"\]"""
  """(ProcessName|process_name)\":\"(?: |({process_path}({process_dir}(?:[^\"]+)?[\\\/])?({process_name}[^\\\/\"]+?)))\""""
  """\"(SubjectUserName)\"\s*:\s*\"(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*\""""
  """\"(SubjectDomainName)\"\s*:\s*\"(-|({domain}.+?))\s*\""""
  """\"(SubjectLogonId)\"\s*:\s*\"(-|({login_id}.+?))\s*\""""
  """\"(ObjectServer)\"\s*:\s*\"(-|({object_server}.+?))\s*\""""
  """\"(ObjectType)\"\s*:\s*\"(-|({object_type}.+?))\s*\""""
  """\"(ObjectName)\"\s*:\s*\"(-|({object}.+?))\s*\""""
  """\"(AccessMask)\"\s*:\s*\"(-|({access}\d*))\s*\""""
  """\"(PrivilegeList)\"\s*:\s*\"(-|({privileges}.+?))\s*\""""
  """({ownership_privilege}SeTakeOwnershipPrivilege)"""
  """record_number\"\s*:\s*\"({event_id}\d+)"""
  """\"ProcessId\\?"+:\\?"+({process_id}[^":\\]+?)\\?""""
  """AccessMask"+:"+((\\)*(\\r|\\t|\\n))*\s*({access_mask}[^\\\s]+)((\\)*(\\r|\\t|\\n))*"""
  """"SubjectUserSid":\"({user_sid}[^\s\"]+)""""
  """"task"+:"+({task_name}[^",]+)""""

  """exa_regex=({event_name}An operation was attempted on a privileged object)"""
  """exa_json_path=$.@timestamp,exa_field_name=time"""
  """exa_json_path=$.hostname,exa_field_name=host"""
  """exa_json_path=$.host,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$"""
  """exa_regex=({event_code}4674)"""
  """exa_json_path=$.keywords,exa_field_name=result"""
  """exa_json_path=$.ProcessName,exa_regex=(?: |({process_path}({process_dir}(?:[^\"]+)?[\\\/])?({process_name}[^\\\/\"]+?)))$"""
  """exa_json_path=$.event_data.SubjectUserName,exa_regex=(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?$"""
  """exa_json_path=$.event_data.SubjectDomainName,exa_regex=(|-|NT Service|NT AUTHORITY|({domain}[^\"]+))\\?$"""
  """exa_json_path=$.event_data.SubjectLogonId,exa_field_name=login_id,exa_match_expr=!InList($..SubjectLogonId,"-")"""
  """exa_json_path=$.event_data.ObjectServer,exa_field_name=object_server,exa_match_expr=!InList($..ObjectServer,"-")""",
  """exa_json_path=$.event_data.ObjectType,exa_field_name=object_type,exa_match_expr=!InList($..ObjectType,"-")""",
  """exa_json_path=$.event_data.ObjectName,exa_field_name=object,exa_match_expr=!InList($..ObjectName,"-")""",
  """exa_json_path=$.event_data.AccessMask,exa_field_name=access,exa_match_expr=!InList($..AccessMask,"-")""",
  """exa_json_path=$.event_data.PrivilegeList,exa_field_name=privileges,exa_match_expr=!InList($..PrivilegeList,"-")""",
  """exa_json_path=$.winlog.event_data.SubjectUserSid,exa_field_name=user_sid"""
  """exa_regex=({ownership_privilege}SeTakeOwnershipPrivilege)"""
  """exa_json_path=$.record_number,exa_field_name=event_id"""
  """exa_json_path=$.ProcessId,exa_regex=({process_id}[^",]*)"""
  """exa_json_path=$.event_data.AccessMask,exa_regex=((\\)*(\\r|\\t|\\n))*\s*({access_mask}[^\\\s]+)((\\)*(\\r|\\t|\\n))*$""",
  """exa_json_path=$.task,exa_field_name=task_name"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```