#### Parser Content
```Java
{
Name = f5-bigipdns-cef-dns-request-success-dnsevent
  ParserVersion = v1.0.0
  Vendor = F5
  Product = F5 BIG-IP DNS
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """CEF:""", """|F5|Advanced Firewall Module|""", """|DNS Event|""", """dpt=53""" ]
  Fields = [
    """rt=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
    """dvchost=({host}[\w\-.]+)""",
    """dvc=({host_ip}[A-Fa-f:\d.]+)""",
    """src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """spt=({src_port}\d+)""",
    """dst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """dpt=({dest_port}\d+)""",
    """cs3=({dns_query_type}.+?)\s*(\w+=|$)""",
    """act=({operation}.+?)\s*(\w+=|$)""",
    """cs4=({dns_query}.+?)\s*(\w+=|$)""",
    """({product_name}Advanced Firewall Module)""",
    """({event_name}DNS Event)""",
  ]


}
```