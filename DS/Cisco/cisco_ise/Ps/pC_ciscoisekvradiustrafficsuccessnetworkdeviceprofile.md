#### Parser Content
```Java
{
Name = "cisco-ise-kv-radius-traffic-success-networkdeviceprofile"
Vendor = "Cisco"
Product = "Cisco ISE"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """, AD-User-Resolved-Identities="""
  """, NetworkDeviceProfileName ="""
]
Fields = [
  """,\s*AD-User-SamAccount-Name =({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """,\s*AD-User-Resolved-Identities=({email_address}[^\s,@]+@[^\s,@]+)"""
  """,\s*AD-User-Join-Point=({domain}[^\s,]+)"""
  """,\s*AuthenticationStatus=({result}[^,]+)"""
  """,\s*NetworkDeviceProfileName =({network}[^,]+)"""
  """,\s*Location=Location#All Locations#({location}[^,]+)"""
  """,\s*EndPointMACAddress=({dest_mac}[^\s,]+)"""
  """, AuthenticationMethod=({auth_type}[^,\s]+)"""
]
ParserVersion = "v1.0.0"


}
```