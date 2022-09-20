#### Parser Content
```Java
{
Name = cisco-ac-cef-vpn-logout-success-stop
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = AnyConnect
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """cisco-av-pair=mdm-tlv=ac-user-agent=AnyConnect""", """Acct-Status-Type=Stop""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d)""",
    """UserName =({user}[^,@\s]+),""",
    """UserName =({full_name}[^,@]+\s\w+)""",
    """Device\sIP\sAddress=({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})""",
    """NetworkDeviceName =({src_host}[^,]+)""",
    """Calling-Station-ID=({dest_host}[^,]+)""",
    """NAS-IP-Address=({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})""",
    """NAS-Port=({dest_port}\d+)""",
    """Acct-Session-Time=({session_duration}[^,]+)""",
    """Acct-Terminate-Cause=({reason}[^,]+)"""
  ]


}
```