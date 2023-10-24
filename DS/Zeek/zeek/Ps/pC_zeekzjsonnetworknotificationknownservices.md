#### Parser Content
```Java
{
Name = zeek-z-json-network-notification-knownservices
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "epoch_sec"
  Conditions = [ """ zeek_known_services """ ]
  Fields = [
    """"ts\\?"+:({time}\d{10})""",
    """"host\\?"+:"+({host}[^"]+)""",
    """"port_num"+:({src_port}\d{13})""",
    """"port_proto"+:"+({protocol}[^"]+)""",
    """"service"+:\["+({service_name}[^"]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```