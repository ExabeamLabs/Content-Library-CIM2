#### Parser Content
```Java
{
Name = "cisco-ise-kv-radius-traffic-fail-failedattempt"
Vendor = "Cisco"
Product = "Cisco Identity and Access Management"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """CISE_Failed_Attempts"""
  """NAS-Port-Type="""
]
Fields = [
  """(::ffff:)?({host}[\w\-.]+) CISE_Failed_Attempts"""
  """, (NetworkDeviceName|NetworkDeviceProfileName)=({network}[^,]+),"""
  """, User-?Name =((host\/)({src_host}[^,]+)|((::ffff:)?(?!(host\/)))?(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|((([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|(({domain}[^\\\/,]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))))"""
  """, NAS-IP-Address=(::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """, Calling-Station-ID=(({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|(::ffff:)?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(::ffff:)?({src_host}[\w\-.]+))"""
  """, SSID=({ssid}[^,]+)"""
  """, Called-Station-ID=({dest_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|(::ffff:)?({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(::ffff:)"""
  """, DestinationIPAddress=(::ffff:)?(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-.]+?)),"""
  """, NAS-Identifier=({computer_name}[\w\-.]+)"""
  """, NetworkDeviceGroups=Location#All Locations#({location}[^,]+)"""
  """, FailureReason=(({result_code}\d+)\s+)?({failure_reason}[^,]+)"""
  """(?i)(MacAddress)=({dest_mac}[^,\s]+),"""
  """, AuthenticationIdentityStore=({auth_server}[^,]+)"""
  """, Device IP Address=(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,"""
  """NAS-IP-Address=({nas_ip_address}[A-Fa-f\d:.]+)"""
  """NOTICE\s+({event_name}[^,]+)""", 
  """\s*Device Port=({src_port}\d+)""",
  """\s*DestinationPort=({dest_port}\d+)"""
  """NAS-IP-Address=({auth_server}[^,]+)"""
  """, NAS-Identifier=({computer_name}[\w\-.]+)"""
]
ParserVersion = "v1.0.0"


}
```