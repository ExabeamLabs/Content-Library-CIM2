#### Parser Content
```Java
{
Name = pfsense-p-csv-network-traffic-fail-block-1
  Vendor = pfSense
  Product = pfSense
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """filterlog""", """,match,block,""" ]
  Fields = [
    """,({dest_interface}[^,]+),({operation}match),({action}block),({direction}\w+),([^,]*,){4,8}((?i)({protocol}UDP|TCP)),([^,]*,){0,2}(::|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){0,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?),(::|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){0,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?),(({=src_port}\d*),({=dest_port}\d*)),({bytes}\d+)"""
    """,({dest_interface}[^,]+),({operation}match),({action}block),({direction}\w+),([^,]*,){4,8}((?i)({protocol}icmpv6|icmp|options|igmp|scmp|sctp)),([^,]*,){1,2}(::|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){0,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?),(::|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){0,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?),"""
  ]


}
```