#### Parser Content
```Java
{
Name = "cisco-ise-kv-endpoint-authentication-accounting"
  Vendor = "Cisco"
  Product = "Cisco ISE"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """ CISE_RADIUS_Accounting """
   ]
  Fields = [
    """({host}\S+) ({event_name}CISE_RADIUS_Accounting)"""
    """CISE_RADIUS_Accounting (\S+\s+){3}({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """User(-)?Name =(?:({user_type}host)/)?(({domain}[^\\\s\/;,@]+)\\+)?(([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2}|({user}[\w\.\-]{1,40}\$?))(;|,|\s)"""
    """User(-)?Name =({user}[\w\.\-]{1,40}\$?)@({domain}[^,;@\s]+)"""
# acct_authentic is removed
# acct_input_octets is removed
# acct_output_octets is removed
    """Acct-Session-Id=({session_id}[^,]+?),"""
    """Acct-Session-Time=({session_duration}[^,]+?),"""
    """AcsSessionID=({acs_session_id}[^,]+?),"""
    """Called-Station-ID=(::ffff:)?(({dest_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
    """Calling-Station-ID=(::ffff:)?(({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
    """Device IP Address=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """Device Type=([^,]*?\#)?({device_type}[^,\#]+?),""",
# framed_ip_address is removed
    """Location=({location}[^,]+?),"""
# nas_identifier is removed
    """NAS-IP-Address=({nas_ip_address}[a-fA-F\d.:]+)"""
# nas_port is removed
# nas_port_type is removed
# networkdevicegroups is removed
# networkdevicename is removed
    """Service-Type=({service_type}[^,]+?),"""
# acct_status_type is removed
    """dhcp-option=host-name=({dest_host}[\w\-\.]+),""",
    """dhcp-option=dhcp-requested-address=({requested_address}[a-fA-F\d:\.]+),"""
  ]
  
  ParserVersion = "v1.0.0"


}
```