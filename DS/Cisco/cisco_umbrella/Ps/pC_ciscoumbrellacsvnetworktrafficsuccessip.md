#### Parser Content
```Java
{
Name = "cisco-umbrella-csv-network-traffic-success-ip"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco"
  Product = "Cisco Umbrella"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
"""destinationServiceName =CiscoUmbrella """
"""dproc=IP """
  ]
  Fields = [
"""({app}CiscoUmbrella)"""
""">\s*"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)","""",
""">\s*"[^"]*","({dest_host}[\w\-\.]+)","""",
""">\s*("[^"]*",){2}"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))","""",
""">\s*("[^"]*",){3}"({src_port}\d+)","""",
""">\s*("[^"]*",){4}"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))","""",
""">\s*("[^"]*",){5}"({dest_port}\d+)","""",
""">\s*("[^"]*",){6}"(|({category}[^"]+))""""  
  ]


}
```