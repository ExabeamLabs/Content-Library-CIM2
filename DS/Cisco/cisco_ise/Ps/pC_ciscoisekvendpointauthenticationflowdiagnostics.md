#### Parser Content
```Java
{
Name = "cisco-ise-kv-endpoint-authentication-flowdiagnostics"
  Vendor = "Cisco"
  Product = "Cisco ISE"
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [
    """ CISE_Authentication_Flow_Diagnostics """
   ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)"""
    """({host}[^\s]+)\s*({event_name}CISE_Authentication_Flow_Diagnostics)"""
    """({event_code}\d+) ({priority}INFO)\s*(Workflow|Authentication):"""
    """, User-?Name =((host\/)({src_host}[^,]+)|((::ffff:)?(?!(host\/)))?(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|((([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|(({domain}[^\\\/,]+)[\\\/]+)?({user}[\w\.\-]{1,40}\$?))))"""
    """AcsSessionID=({acs_session_id}[^,]+),"""
    """AuthenticationMethod=({auth_method}[^,]+?),"""
    """Calling-Station-ID=(::ffff:)?(({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
    """DestinationIPAddress=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """NAS-IP-Address=(::ffff:)?({nas_ip_address}[a-fA-F\d.:]+)"""
    """Response=\{({response}[^,]+?)\s*\},"""
    """INFO\s*({event_name}(Authentication|Workflow):[^,]+),"""
  ]
  ParserVersion = "v1.0.0"


}
```