#### Parser Content
```Java
{
Name = "cisco-ise-kv-radius-traffic-success-accountstartreq"
Vendor = "Cisco"
Product = "Cisco Identity and Access Management"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS Z"
Conditions = [
  """Acct-Status-Type=Start"""
  """Acct-Authentic=RADIUS"""
  """RADIUS Accounting start request"""
]
Fields = [
  """CISE_RADIUS_Accounting[^,]+?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d [+-]\d\d:\d\d)"""
  """({host}[\w\-.]+) CISE_RADIUS_Accounting"""
  """Host:\s*({host}\S+)"""
  """, NetworkDeviceName =({network}[^,]+),"""
  """, User-?Name =((host\/)({src_host}[^,]+)|(?!(host\/))((({domain}[^\\\/,\s@]+)[\\\/]+)?(([a-fA-f\d]{1,2}(\-|:)){5}[a-fA-f\d]{1,2}|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))),"""  
  """, User-?Name =({email_address}[^\\\/\s,@]+@[^\\\/\s,@]+\.[^\]\s"\\,\|]+)"""
  """, NAS-Identifier=({computer_name}[\w\-.]+)"""
  """, Device IP Address=({auth_server}[^,]+)"""
  """, Device IP Address=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """, Framed-IP-Address=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """, NAS-Identifier=({dest_host}[\w\-.]+)"""
  """, Called-Station-ID=(({dest_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|({dest_host}[\w\-.]+))(:({ssid}[^,:]+)?),"""
  """, Calling-Station-ID=(({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
  """, NetworkDeviceGroups=Location#All Locations#({location}[^,]+)"""
  """(?i)(MacAddress)=({src_mac}[^,\s]+),"""
  ]
ParserVersion = "v1.0.0"


}
```