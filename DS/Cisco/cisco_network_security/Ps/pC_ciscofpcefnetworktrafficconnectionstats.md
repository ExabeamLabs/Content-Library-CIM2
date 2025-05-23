#### Parser Content
```Java
{
Name = "cisco-fp-cef-network-traffic-connection-stats"
  Vendor = "Cisco"
  ParserVersion = "v1.0.0"
  Product = Cisco Network Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
    """|Cisco|"""
    """|Firepower|"""
    """|CONNECTION STATISTICS|"""
  ]
  Fields = [
    """@timestamp[\":]*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""
    """\"host[\":]*({host}[^\"]+)"""
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """act=({action}[^\s]+)"""
    """reason=(?:N\/A|({failure_reason}[^\s]+))"""
    """deviceInboundInterface=({src_interface}[^\s]+)\s*deviceOutboundInterface=({dest_interface}[^\s]+)"""
    """app=(?:Unknown|({app}[^\s]+))"""
    """bytesIn=({bytes_in}\d+)\s*bytesOut=({bytes_out}\d+)"""
    """proto=({protocol}[^\s]+)"""
    """cs1=({policy_name}[^\s]+)"""
    """cs2=({rule}[^\s]+)"""
    """cs5Label=({category}[^\s]+)"""
    """dpt=({dest_port}\d+)\s*dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({=dest_port}\d+))?"""
    """request=({url}[^\s]+)"""
    """spt=({src_port}\d+)\s*src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({=src_port}\d+))?"""
    """user=(?:No Authentication Required|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  ]


}
```