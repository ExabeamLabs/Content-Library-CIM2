#### Parser Content
```Java
{
Name = juniper-ps-mix-vpn-login-fail-hostchecker
  Vendor = Juniper Networks
  Product = Juniper Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Host Checker policies could not be evaluated on host""" ]
  Fields = [
    """ on host '({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s+PulseSecure:\s+({time}\d\d\d\d\-\d\d-\d\d \d\d:\d\d:\d\d)\s+(\S+\s+){3}\[\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}\]\s+({user}[^\s\(\)]+)\((?:unknown|({realm}[^)]+))\)""",
    """user=({user}[^\s]+)""",
    """src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
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