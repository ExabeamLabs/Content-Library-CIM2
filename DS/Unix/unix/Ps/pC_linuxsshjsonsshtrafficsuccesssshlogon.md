#### Parser Content
```Java
{
Name = "linux-ssh-json-ssh-traffic-success-sshlogon"
Vendor = "Unix"
Product = "Unix"
TimeFormat = "yyyy-MM-dd HH:mm:ss.S"
Conditions = [
  """SSH_Logon_"""
  """USER_TEXT: """
  """COLLECTORNAME: """
  """ ASSET_COLLECTORRID: """
  """SVA_IP_ADDRESS: """
]
Fields = [
  """EVENT_DT:\s\"+({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\.\d)\""""
  """\sHOSTADDR:\s\"+({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\""""
  """\sHOSTNAME:\s+\"+({host}[^\"]+)\"+\s"""
  """Remote From:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\sDESCRIPTION:\s\"+({description}[^\"]+)\""""
  """OSTYPE_D:\s\"+({os}[^\"]+)\"+\s"""
  """Session id:\s*({session_id}\d+)"""
  """Process Name:\s*(null|unknown|({process_name}\S+))"""
  """Parent Name:\s*(null|unknown|({parent_process_name}\S+))"""
  """Username:\s*({user}[\w\.\-]{1,40}\$?)"""
  """Port:\s*({src_port}\d+)"""
  """\sRULE_NAME: \"*({rule}[^\"]+)\""""
  """EVENT_TYPE_D:\s+\"+({event_name}[^\"]+)\"+\s"""
  """EVENT_ID:\s+\"+({login_id}[^\"]+)\"+\s"""
  """PROCESS_ID:\s+\"+(null|unknown|({process_id}[^\"]+))\"+\s"""
]
DupFields = [
  "event_name->event_category"
]
ParserVersion = "v1.0.0"


}
```