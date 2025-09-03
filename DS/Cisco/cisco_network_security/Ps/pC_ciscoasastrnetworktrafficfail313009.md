#### Parser Content
```Java
{
Name = cisco-asa-str-network-traffic-fail-313009
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = ["MMM dd yyyy HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ """Denied invalid ICMP code """, """-313009""" ]
  Fields = [
    """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
    """({time}\w{3}\s+\d+\s+(\d+\s+)?\d\d:\d\d:\d\d)\s(\S+\s+):\s+%\w+\-"""
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%\w+\-""",
    """({host}[\w\-.]+)?\s*({time}\w{3} \d+ \d{4} \d\d:\d\d:\d\d)\s*({=host}[\w\-.]+)?\s*:\s*%ASA\-({priority}\d+)\-({event_code}\d+)""",
    """for\s+({src_interface}[^:]+):\s*(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))\/({src_port}\d+)\s*\(({src_translated_ip}[a-fA-F:\d.]+)\/({src_translated_port}\d+)""",
    """to\s+({dest_interface}[^:]+):\s*(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))\/({dest_port}\d+)\s*\(({dest_translated_ip}[a-fA-F:\d.]+)\/({dest_translated_port}\d+)""",
    """({event_name}Denied invalid ICMP code)""",
    """({protocol}ICMP)"""
  ]


}
```