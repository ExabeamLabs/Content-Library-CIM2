#### Parser Content
```Java
{
Name = juniper-ps-mix-vpn-login-fail-hostchecker
  Vendor = Ivanti
  Product = Ivanti Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Host Checker policies could not be evaluated on host""" ]
  Fields = [
    """ on host '({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+PulseSecure:\s+({time}\d\d\d\d\-\d\d-\d\d \d\d:\d\d:\d\d)\s+(\S+\s+){3}\[\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}\]\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\((?:unknown|({realm}[^)]+))\)""",
    """user=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """proto=({protocol}[^\s]+)""",
    """msg="+({additional_info}[^"]+)""",
    """\Wfw=({firewall}[a-fA-F\d.:]+)""",
    """vpn=({host}[^\s]+)""",
    """time="+({time}[^"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```