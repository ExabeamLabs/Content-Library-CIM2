#### Parser Content
```Java
{
Name = "cisco-asa-str-network-traffic-fail-313004"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco"
  Product = Cisco Network Security
  TimeFormat = ["MMM dd yyyy HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ","MMM dd HH:mm:ss","MMM d HH:mm:ss", "MMM  d HH:mm:ss"]
  Conditions = [ """Denied ICMP """, """-313004""", """ type=""", """, from laddr """ ]
  Fields = [
    """({time}\w{3}\s+\d+(\s\d+)?\s\d\d:\d\d:\d\d)\s""",
    """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
    """\s(({host}[\w.\-]+))\s+:\s*(\w+\s|%\w+\-)""",
    """\d\d:\d\d:\d\d\s(\w+\s)?({host}[\w\-.]+)\s*:\s*(\w+\s|%\w+\-)(|\w+\-)?({priority}\d+)\-({event_code}\d+)""",
    """(({host}[\w\-.]+)\s+)?({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d).*?%\w+\-({priority}\d+)\-({event_code}\d+)""",
    """from laddr\s*(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({src_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?)) on interface\s*({src_interface}\S+)""",
    """to \s*(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({dest_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?)):\s*({result_reason}[^"]+?)\s*("|$)""",
    """({event_name}Denied ICMP)""",
    """-313004:Denied\s*({protocol}\S+)"""
  ]


}
```