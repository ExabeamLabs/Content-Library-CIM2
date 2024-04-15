#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-privilege-use-success-4674-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """An operation was attempted on a privileged object."""
  """"event_id":4674"""
  """"@timestamp""""
]
Fields = [
  """({event_name}An operation was attempted on a privileged object)"""
  """\"@timestamp\"\s*:\s*\"({time}.+?)\""""
  """\"hostname\":\"({host}[^.\"]*)"""
  """\"host\":\"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """({event_code}4674)"""
  """\"keywords\":\[\"({action}.+?)\"\]"""
  """process_name\":\"(?: |({process_path}({process_dir}(?:[^\"]+)?[\\\/])?({process_name}[^\\\/\"]+?)))\""""
  """\"(SubjectUserName)\"\s*:\s*\"(-|({user}.+?))\s*\""""
  """\"(SubjectDomainName)\"\s*:\s*\"(-|({domain}.+?))\s*\""""
  """\"(SubjectLogonId)\"\s*:\s*\"(-|({login_id}.+?))\s*\""""
  """\"(ObjectServer)\"\s*:\s*\"(-|({object_server}.+?))\s*\""""
  """\"(ObjectType)\"\s*:\s*\"(-|({object_type}.+?))\s*\""""
  """\"(ObjectName)\"\s*:\s*\"(-|({object}.+?))\s*\""""
  """\"(AccessMask)\"\s*:\s*\"(-|({access}\d*))\s*\""""
  """\"(PrivilegeList)\"\s*:\s*\"(-|({privileges}.+?))\s*\""""
  """({ownership_privilege}SeTakeOwnershipPrivilege)"""
  """record_number\"\s*:\s*\"({event_id}\d+)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```