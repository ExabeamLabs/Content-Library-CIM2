#### Parser Content
```Java
{
Name = "cisco-ise-kv-radius-traffic-fail-failedattempt"
Vendor = "Cisco"
Product = "Cisco ISE"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """CISE_Failed_Attempts"""
  """NAS-Port-Type="""
]
Fields = [
  """(::ffff:)?({host}[\w\-.]+) CISE_Failed_Attempts"""
  """, (NetworkDeviceName|NetworkDeviceProfileName)=({network}[^,]+),"""
  """, User-?Name =((host\/)({src_host}[^,]+)|((::ffff:)?(?!(host\/)))?(({email_address}[^,@]+@[^,@\s]+\.[^,@\s]+)|((([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|(({domain}[^\\\/,]+)[\\\/]+)?({user}[^\\\/\s,]+))))"""
  """, NAS-IP-Address=(::ffff:)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """, DestinationIPAddress=(::ffff:)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """, Calling-Station-ID=(({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|(::ffff:)?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(::ffff:)?({src_host}[\w\-.]+))"""
  """, SSID=({ssid}[^,]+)"""
  """, Called-Station-ID=(({dest_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|(::ffff:)?({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(::ffff:)?({dest_host}[\w\-.]+))(:({ssid}[^,]+))?,"""
  """, NAS-Identifier=(::ffff:)?({dest_host}[\w\-.]+)"""
  """, NAS-Identifier=({computer_name}[\w\-.]+)"""
  """, NetworkDeviceGroups=Location#All Locations#({location}[^,]+)"""
  """, FailureReason=(({failure_code}\d+)\s+)?({failure_reason}[^,]+)"""
  """(?i)(MacAddress)=({dest_mac}[^,\s]+),"""
  """, AuthenticationIdentityStore=({auth_server}[^,]+)"""
  """, Device IP Address=({auth_server}[^,]+)"""
  """, Device IP Address=(::ffff:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,"""
  """NAS-IP-Address=({nas_ip_address}[A-Fa-f\d:.]+)"""
  """NOTICE\s+({event_name}[^,]+)""", 
]
ParserVersion = "v1.0.0"


}
```