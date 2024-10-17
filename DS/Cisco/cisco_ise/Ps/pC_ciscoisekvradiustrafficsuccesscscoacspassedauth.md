#### Parser Content
```Java
{
Name = "cisco-ise-kv-radius-traffic-success-cscoacspassedauth"
Vendor = "Cisco"
Product = "Cisco ISE"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS Z"
Conditions = [
  """Passed-Authentication: Authentication succeeded"""
  """CSCOacs_Passed_Authentications"""
  """ACSVersion="""
]
Fields = [
  """\s({host}[\w\-.]+)\s+CSCOacs_Passed_Authentications"""
  """\s+\d+\s+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d\s(\+|-)\d\d:\d\d)"""
  """, User-?Name =((host\/)({src_host}[^,]+)|((::ffff:)?(?!(host\/)))?(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|((([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|(({domain}[^\\\/,]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))))"""
  """,\s*User-?Name =(?=[^\s]+@[^\s]+)({email_address}[^\s,]+)"""
  """,\s*Calling-Station-ID=({dest_host}[^,]+)"""
  """,\s*NAS-Identifier=({dest_host}[^@,]+)"""
  """,\s*NAS-Identifier=({computer_name}[^@,]+)"""
  """,\s*Device IP Address=({auth_server}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """,\s*Device IP Address=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """,\s*Framed-IP-Address=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """,\s*SelectedAuthorizationProfiles=({access_type}[^,]+)"""
  """,\s*AuthenticationMethod=({auth_type}[^,]+)"""
]
ParserVersion = "v1.0.0"


}
```