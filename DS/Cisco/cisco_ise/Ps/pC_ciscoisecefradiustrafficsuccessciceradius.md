#### Parser Content
```Java
{
Name = cisco-ise-cef-radius-traffic-success-ciceradius
  Vendor = Cisco
  Product = Cisco ISE
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = ["""CISE_RADIUS_Accounting""", """CEF:0|Cisco|Cisco ISE|"""]
  Fields = [
    """dvchost=({host}\S+)"""
    """({event_name}CISE_RADIUS_Accounting)""",
    """({time}\w+ \d+ \d\d:\d\d:\d\d)""",
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)""",
    """duser=(?:({user_type}host)/)?(({domain}[^\\\s\/;,@]+)\\+)?({user}[^,;@\s\\\/]+)(;|,|\s)""",
    """User(-)?Name =({email_address}[^,;@\s]+@[^,;@\s]+)""",
# acct_authentic is removed
# acct_input_octets is removed
# acct_output_octets is removed
    """ad\.Acct-Session-Id=({session_id}.+?)\s+[\w\.-]+=""",
    """ad\.Acct-Session-Time=({session_duration}.+?)\s+[\w\.-]+=""",
    """ad.AcsSessionID=({session_id}.+?)\s+[\w\.-]+=""",
# called_station_id is removed
    """ad.Calling-Station-ID=({calling_station_id}.+?)\s+[\w\.-]+=""",
# device_ip_address is removed
    """ad.Device_,Type=({device_type}.+?)\s+[\w\.-]+=""",
# framed_ip_address is removed
    """ad.Location=({location}.+?)\s+[\w\.-]+=""",
# nas_identifier is removed
    """ad\.NAS-IP-Address=({nas_ip_address}[a-fA-F\d.:]+)""",
# nas_port is removed
# nas_port_type is removed
# networkdevicegroups is removed
# networkdevicename is removed
    """smac=({src_mac}.+?)\s+[\w\.-]+=""",
  ]


}
```