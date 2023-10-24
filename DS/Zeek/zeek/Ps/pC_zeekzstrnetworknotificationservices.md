#### Parser Content
```Java
{
Name = zeek-z-str-network-notification-services
  Vendor = Zeek
  Product = Zeek 
  TimeFormat = "epoch_sec"
  Conditions = [ """/known_services.log""" ]
  Fields = [
# Dl Fields are removed
    """({time}\d{10})\.\d{6}\s+({host}[^\s]+)\s+((\d+?)|[^\s]+)\s+([^\s]+)\s+({service_name}[^\s]+?)\s*"""
  ]
  DupFields = [ "port_num->src_port", "port_proto->protocol" ]
  ParserVersion = "v1.0.0"


}
```