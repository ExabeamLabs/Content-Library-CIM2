#### Parser Content
```Java
{
Name = pfsense-p-csv-network-traffic-fail-block
  ParserVersion = v1.0.0
  Vendor = pfSense
  Product = pfSense
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """filterlog:""", """,match,block,""" ]
  Fields = [
    """filterlog:(?:[^,]*,){4}({dest_interface}[^,]*),({operation}[^,]*),({action}[^,]*),({direction}[^,]*),(?:[^,]*,){8}({protocol}(tcp|udp)),[^,]*,({src_ip}[^,]*),({dest_ip}[^,]*),({src_port}\d*),({dest_port}\d*),""",
    """filterlog:(?:[^,]*,){7}in,(?:[^,]*,){8}(tcp|udp),(?:[^,]*,){5}({bytes_in}\d+)""",
    """filterlog:(?:[^,]*,){4}({dest_interface}[^,]*),({operation}[^,]*),({action}[^,]*),({direction}[^,]*),(?:[^,]*,){8}({protocol}icmp),[^,]*,({src_ip}[^,]*),({dest_ip}[^,]*),"""
  ]


}
```