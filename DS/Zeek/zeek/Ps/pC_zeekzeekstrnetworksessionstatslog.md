#### Parser Content
```Java
{
Name = zeek-zeek-str-network-session-statslog
  ParserVersion = v1.0.0
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "epoch_sec"
  Conditions = [ """/stats.log""" ]
  Fields = [
    """({time}\d{10})\.\d{6}[\s\t]*"""
# active_dns_requests is removed
  ]


}
```