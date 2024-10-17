#### Parser Content
```Java
{
Name = "cisco-ise-kv-radius-traffic-success-tacacsaccouting"
Vendor = "Cisco"
Product = "Cisco ISE"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS Z"
Conditions = [
  """ CISE_TACACS_Accounting """
  """ TACACS+ Accounting START"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d (\+|-)\d\d:\d\d)"""
  """({host}[^\s]+)\s*CISE_TACACS_Accounting"""
  """({event_name}CISE_TACACS_Accounting)"""
  """Host:\s*({host}\S+)"""
  """, NetworkDeviceName =({src_host}[^,]+),"""
  """, Device IP Address=({auth_server}[^,]+)"""
  """, Device IP Address=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """, NetworkDeviceGroups=Location#All Locations#({location}[^,]+)"""
  """\sService=((?i)None|({service_name}[^,]+))"""
  """\sUser=(({email_address}[^\s]+?@[^\s]+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),"""
  """\sRemote-Address=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """\sPort=({src_port}\d+)"""
  """\sAuthen-Method=({auth_method}[^,]+)"""
  """\sAcsSessionID=({session_id}[^,]+)"""
]
ParserVersion = "v1.0.0"


}
```