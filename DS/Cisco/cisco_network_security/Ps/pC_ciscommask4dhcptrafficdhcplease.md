#### Parser Content
```Java
{
Name = "cisco-mma-sk4-dhcp-traffic-dhcplease"
  Vendor = "Cisco"
  Product = Cisco Network Security
  TimeFormat = "epoch_sec"
  Conditions = [
    """ events dhcp lease of ip """
    """ from router """
    """ for client mac """
    """ on subnet """
  ]
  Fields = [
     """({time}\d{10})\.\d+\s+({host}[\w.\-]+) events ({event_name}dhcp lease) of ip ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))? from \w+ mac (\S+) for client mac ({src_mac}\S+) from router (\S+) on subnet ({router_subnet}\S+) with dns ([a-fA-F\d.:]+)"""# DL Fields are removed
  ]
  ParserVersion = "v1.0.0"


}
```