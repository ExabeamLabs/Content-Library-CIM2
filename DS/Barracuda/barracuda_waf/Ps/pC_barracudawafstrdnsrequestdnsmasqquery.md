#### Parser Content
```Java
{
Name = barracuda-waf-str-dns-request-dnsmasqquery
  ParserVersion = v1.0.0
  Vendor = Barracuda
  Product = Barracuda WAF
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """ dnsmasq[""", """: query""", """ from """ ]
  Fields = [
    """({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d+\s*(\+|\-)[\d:]+)"""
    """query\S+\s+({dns_query}.*?)\s+from\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """({app}dnsmasq)"""
  ]


}
```