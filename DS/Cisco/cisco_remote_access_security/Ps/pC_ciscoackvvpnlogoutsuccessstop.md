#### Parser Content
```Java
{
Name = cisco-ac-kv-vpn-logout-success-stop
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Remote Access Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS Z"
  Conditions = [ """RADIUS Accounting stop request""", """Acct-Status-Type=Stop""" ]
  Fields = [
    """\s({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d\d\d\s[+-]\d\d:\d\d)\s""",
    """({event_name}RADIUS Accounting stop request)""",
    """, User-?Name =((host\/)({src_host}[^,]+)|((::ffff:)?(?!(host\/)))?(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|((([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|(({domain}[^\\\/,]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))))""",
    """Acct-Session-Id=({session_id}\w+),""",
    """Acct-Session-Time=({session_duration}\d+),""",
    """AcsSessionID=({acs_session_id}[^,]+?),""",
    """Called-Station-ID=(::ffff:)?(({dest_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """Calling-Station-ID=(::ffff:)?(({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """Device IP Address=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """NAS-IP-Address=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """Service-Type=({service_type}[^,]+?),""",
    """NetworkDeviceName =({src_host}[^,]+)""",
    """Acct-Terminate-Cause=({result_reason}[^,]+)"""
    """({result}Stop)"""
  ]


}
```