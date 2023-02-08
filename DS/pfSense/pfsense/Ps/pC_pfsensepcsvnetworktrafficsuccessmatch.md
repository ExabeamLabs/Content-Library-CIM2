#### Parser Content
```Java
{
Name = pfsense-p-csv-network-traffic-success-match
  Vendor = pfSense
  Product = pfSense
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """filterlog""", """,match,pass,""" ]
  Fields = [
    """filterlog:?(?:[^,]*,){4}({dest_interface}[^,]*),({operation}[^,]*),({action}[^,]*),({direction}[^,]*),(?:[^,]*,){8}({protocol}(tcp|udp)),[^,]*,({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?,({=src_port}\d*),({=dest_port}\d*),""",
    """filterlog:?(?:[^,]*,){7}in,(?:[^,]*,){8}(tcp|udp),(?:[^,]*,){5}({bytes_in}\d+)""",
    """filterlog:?(?:[^,]*,){4}({dest_interface}[^,]*),({operation}[^,]*),({action}[^,]*),({direction}[^,]*),(?:[^,]*,){8}({protocol}icmp),[^,]*,({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?,"""
  ]
   DupFields = [ "host->dest_host"]
   ParserVersion = "v1.0.0"


}
```