#### Parser Content
```Java
{
Name = unix-dhcpd-csv-dhcp-traffic-expired
  Vendor = Unix
  Product = Unix dhcpd
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  ParserVersion = "v1.0.0"
  Conditions = [ """,Expired,""" ]
  Fields = [
    """,({event_name}Expired),({src_ip}((([0-9a-fA-F.:]{1,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,({src_host}[^,]+)?""",
  ]


}
```