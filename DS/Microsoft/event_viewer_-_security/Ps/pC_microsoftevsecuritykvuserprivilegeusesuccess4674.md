#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-privilege-use-success-4674"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """__li_source_path="""
  """An operation was attempted on a privileged object"""
  """eventid="4674""""
]
Fields = [
  """({event_name}An operation was attempted on a privileged object)"""
  """__li_source_path="({host}(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-.]+)))"""",
  """({event_code}4674)"""
  """(K|k)eywords=\"({result}[^\"]+)\""""
  """Process Name:\s+(?: |({process_path}({process_dir}(?:[^\"]+)?[\\\/])?({process_name}[^\\\/\"]+?)))\s+Requested"""
  """(?:Information|Success Audit|Audit Success).+?Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain:"""
  """\s+Account Domain:\s+({domain}.+?)\s+Logon ID:\s+({login_id}[^\s]+)"""
  """Object Server:\s+({object_server}.+?)\s+Object Type:\s+(?:-|({object_type}.+?))\s+Object Name:\s+(?:-|({object}.+?))\s+Object Handle"""
  """Desired Access:\s+({access}.+?)\s+Privileges:\s+({privileges}.+?)(,\d+|\s*$)"""
  """\s+({ownership_privilege}SeTakeOwnershipPrivilege)"""
  """\s+({environment_privilege}SeSystemEnvironmentPrivilege)"""
  """\s+({debug_privilege}SeDebugPrivilege)"""
  """\s+({tcb_privilege}SeTcbPrivilege)"""
]
ParserVersion = "v1.0.0"


}
```