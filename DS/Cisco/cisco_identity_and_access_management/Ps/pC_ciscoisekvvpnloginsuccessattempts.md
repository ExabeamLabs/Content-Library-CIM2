#### Parser Content
```Java
{
Name = "cisco-ise-kv-vpn-login-success-attempts"
Vendor = "Cisco"
Product = "Cisco Identity and Access Management"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """CSCOacs_Failed_Attempts"""
  """Failed-Attempt: Authentication failed"""
  """NAS-Port-Type=Virtual"""
]
Fields = [
  """\d+\s+({time}\d\d\d\d\-\d\d\-\d\d \d+:\d+:\d+)"""
  """CSCOacs_Failed_Attempts\s+(\d+\s+){3}\s+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
  """({dest_host}[^\s]+)\s+CSCOacs_Failed_Attempts"""
  """,\s*User-Name =(({domain}[^\s\\\/]+)(\/+|\\+))?(?:(\w{2}\-){5}\w{2}|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """Tunnel-Client-Endpoint=\(.+\)\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """Framed-IP-Address=({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),"""
  """,\s*Device IP Address=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\WFailed-Attempt:\s*({failure_reason}[^,]+)"""
  """\s*DestinationIPAddress=({auth_server}[a-fA-F\d.:]+)"""
  """\s*Device Port=({dest_port}\d+)"""
  """AcsSessionID=({session_id}[^,]+)"""
  """({event_name}CSCOacs_Failed_Attempts)"""
  """device-platform=({os}[^,\s]+)"""
  """device-platform-version=({os_version}[^,\s]+)"""
  """Group-Name =({realm}[^,\s]+)"""
  """\s*ConfigVersionId=({badge_id}\d+)"""
  """({event_code}5400)"""
]
DupFields = [
  "user->account"
]
ParserVersion = "v1.0.0"


}
```