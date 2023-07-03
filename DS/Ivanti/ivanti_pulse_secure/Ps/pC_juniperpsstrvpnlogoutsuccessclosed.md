#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-logout-success-closed
  ParserVersion = v1.0.0
  Vendor = Ivanti
  Product = Ivanti Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
""" Closed connection to """
""" bytes read """
""" bytes written """
]
  Fields = [
    """:\s*({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})\s""",
    """Juniper:\s({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)\s\S\s({host}[\w\-.]+)""",
    """\w{3}\s+\d{1,2}\s+\d{2}:\d{2}:\d{2}\s+({host}[\w\.-]+)\s+\S*?[\[:\s]""",    
    """- \[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))]\s+([\w\s]+?::)?(?:({domain}\w+)\\)?(({email_address}[^@]+@[^\s]+?)|({user}[^\(\[]+?))[\(\[]""",
    """Closed connection to (?:({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))""",
    """- Closed connection to \S+\s+port ({dest_port}\d+)""",
    """\safter\s+({session_duration}\d+)\s+seconds""",
    """\swith\s+({bytes_in}\d+)\s+bytes read""",
    """\sand\s+({bytes_out}\d+)\s+bytes written"""
  ]


}
```