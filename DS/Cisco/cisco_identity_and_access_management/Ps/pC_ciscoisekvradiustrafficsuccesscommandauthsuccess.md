#### Parser Content
```Java
{
Name = "cisco-ise-kv-radius-traffic-success-commandauthsuccess"
Vendor = "Cisco"
Product = "Cisco Identity and Access Management"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS Z"
Conditions = [
  """Device-Administration: Command Authorization succeeded"""
  """CSCOacs_Passed_Authentications"""
]
Fields = [
  """({host}[\w.\-]+)\s+CSCOacs_Passed_Authentications(\s+\S+){3}\s+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+ (\+|\-)\d\d:\d\d)"""
  """Device-Administration:\s*({event_name}[^,]+)"""
  """, Device IP Address=({auth_server}[^,]+)"""
  """, DestinationIPAddress=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """, DestinationPort=({dest_port}\d+)"""
  """, UserName =({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """, Protocol=({protocol}[^,]+)"""
  """, Remote-Address=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """, AuthenticationMethod=({auth_type}[^,]+)"""
]
ParserVersion = "v1.0.0"


}
```