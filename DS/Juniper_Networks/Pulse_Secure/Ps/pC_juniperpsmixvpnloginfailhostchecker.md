#### Parser Content
```Java
{
Name = juniper-ps-mix-vpn-login-fail-hostchecker
  Vendor = Juniper Networks
  Product = Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Host Checker policies could not be evaluated on host""" ]
  Fields = [
    """ on host '({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s+PulseSecure:\s+({time}\d\d\d\d\-\d\d-\d\d \d\d:\d\d:\d\d)\s+(\S+\s+){3}\[\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}\]\s+({user}[^\s\(\)]+)\((?:unknown|({realm}[^)]+))\)""",
    """user=({user}[^\s]+)""",
    """src=({src_ip}[A-Fa-f:\d.]+)""",
    """proto=({protocol}[^\s]+)""",
    """msg="+({additional_info}[^"]+)""",
    """\Wfw=({firewall}[a-fA-F\d.:]+)""",
    """vpn=({host}[^\s]+)""",
    """time="+({time}[^"]+)"""
  ]
  DupFields = [ "dest_ip->host" ]
  ParserVersion = "v1.0.0"


}
```