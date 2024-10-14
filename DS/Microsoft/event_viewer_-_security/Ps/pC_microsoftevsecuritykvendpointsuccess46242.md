#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-success-4624-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """__li_source_path="""
  """An account was successfully logged on"""
  """eventid="4624""""
]
Fields = [
  """({event_name}An account was successfully logged on)"""
  """__li_source_path="({host}[\w\-.]+)""""
  """__li_source_path="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
  """({event_code}4624)"""
  """Logon Type:\s*({login_type}\d+)"""
  """New Logon.*Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain:\s+({domain}[\w.\-]+)"""
  """Process Name:\s+(?:-|({process_path}[\w:\\.\-]+))"""
  """Source Network Address:\s+(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s+Source Port:"""
  """Logon Process:\s*({auth_process}[^\s]+)\s+Authentication Package:\s*({auth_package}[^\s]+)"""
  """Logon ID:\s+({login_id}[^\s]+)\s+Logon GUID"""
  """New Logon:\s+Security ID:\s+({user_sid}[^\s]+)\s"""
  """Workstation Name:\s+([A-Fa-f:\d.]+|({src_host_windows}[^\s]+))\s+Source Network"""
  """Key Length:\s+({key_length}\d+)\s"""
]
DupFields = [ "src_host_windows->src_host" ]
ParserVersion = "v1.0.0"


}
```