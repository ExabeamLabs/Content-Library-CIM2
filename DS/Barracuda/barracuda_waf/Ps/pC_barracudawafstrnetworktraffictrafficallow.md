#### Parser Content
```Java
{
Name = barracuda-waf-str-network-traffic-trafficallow
  ParserVersion = v1.0.0
  Vendor = Barracuda
  Product = Barracuda WAF
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS Z"
  Conditions = [ """ ALLOW """, """ traffic:allow""", """ ACL""", """ interface """ ]
  Fields = [
    """({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2}\.\d+\s*(\+|\-)[\d:]+)"""
    """({host}[\w.-]+)\s+(\S+)\s+({severity}\S+)\s+({protocol}\S+)\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+({src_port}\d+)\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+({dest_port}\d+)\s+({action}ALLOW)\s+"""
  ]


}
```