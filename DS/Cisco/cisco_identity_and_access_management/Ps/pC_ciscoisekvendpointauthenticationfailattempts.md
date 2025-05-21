#### Parser Content
```Java
{
Name = cisco-ise-kv-endpoint-authentication-fail-attempts
  Vendor = Cisco
  Product = Cisco Identity and Access Management
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """CISE_Failed_Attempts""", """since user has entered the wrong password""" ]
  Fields = [
    """({host}[\w\-.]+)\s+CISE_Failed_Attempts""",
    """\d+\s+({time}\d\d\d\d\-\d\d\-\d\d \d+:\d+:\d+)""",
    """, User-?Name =((host\/)({src_host}[^,]+)|((::ffff:)?(?!(host\/)))?(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|((([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|(({domain}[^\\\/,]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))))"""
    """, Calling-Station-ID=({dest_host}[^,]+)""",
    """, Called-Station-ID=({src_host}[^,]+):({ssid}[^,]+)""",
    """, AD-Host-Resolved-Identities=({dest_host}[^@,]+)""",
    """, AD-Host-Resolved-Identities=({computer_name}[^@,]+)""",
    """, (NetworkDeviceName|NetworkDeviceProfileName)=({network}[^,]+)""",
    """, Device IP Address=({auth_server}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """, Device IP Address=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """, Framed-IP-Address=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """, DestinationIPAddress=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """, NetworkDeviceGroups=Location#All Locations#({location}[^,]+)""",
    """, FailureReason=({result_code}\d+)""",
    """, FailureReason=\d+ ({failure_reason}[^,]+)""",
    """(?i)(MacAddress)=({src_mac}[^,\s]+),""",
    """, SSID=({ssid}[^,]+)""",
    """, AuthenticationIdentityStore=({auth_server}[^,]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```