#### Parser Content
```Java
{
Name = "observeit-o-kv-endpoint-login-success-observeitsessions"
Vendor = "Proofpoint"
Product = "ObserveIT"
TimeFormat = "MM/dd/yyyy HH:mm:ss"
Conditions = [
  """EventName =ObserveIT-Sessions;"""
]
Fields = [
  """({host}\S+)\s+(\S+\s+){4}EventName ="""
  """\sSessionDate=({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d)"""
  """\sOS=({os}[^;]+?)\s*(;|"*\s*$)"""
  """\sSessionID=({session_id}[^;]+?)\s*(;|"*\s*$)"""
  """\sServerName =({dest_host}[^;]+?)\s*(;|"*\s*$)"""
  """\sDomainName =({domain}[^;]+?)\s*(;|"*\s*$)"""
  """\sUserName =(?:n\/a|({user}[\w\.\-]{1,40}\$?))\s*(;|"*\s*$)"""
  """\sLoginName =({user}[\w\.\-]{1,40}\$?)\s*(;|"*\s*$)"""
  """\sClientAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\sViewerURL=({additional_info}[^;]+?)\s*(;|"*\s*$)"""
]
ParserVersion = "v1.0.0"


}
```