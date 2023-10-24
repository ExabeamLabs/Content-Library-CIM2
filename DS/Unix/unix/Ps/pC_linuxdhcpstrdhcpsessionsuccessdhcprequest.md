#### Parser Content
```Java
{
Name = "linux-dhcp-str-dhcp-session-success-dhcprequest"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """ DHCPREQUEST for """
    """ from """
    """ via """
  ]
  Fields = [
    """\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+dhcpd(\[\d+\])?:\s+DHCPREQUEST for ({dest_ip}[a-fA-F\d\.:]+)\s.*?from ({dest_mac}[a-fA-F\d\.:]+)(\s\(({dest_host}[^\)]+?)(-.*?)?\))?( via (({src_ip}[\d.:a-fA-F]+[\da-fA-F]):?|({dest_interface}[\w-]+)))\s*"""
    """for\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  DupFields = [
    "host->auth_server"
  ]
  ParserVersion = "v1.0.0"


}
```