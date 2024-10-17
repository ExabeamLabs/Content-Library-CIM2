#### Parser Content
```Java
{
Name = cisco-asa-str-network-session-success-713903
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = ["MMM dd yyyy HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  ParserVersion = "v1.0.0"
  Conditions = [ """-713903""", """%ASA-""" ]
  Fields = [
    """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
"""\s(({host}[\w.\-]+))\s+([-\s:]+)?%ASA""",
    """(({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s*)?({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)""",
    """%ASA\-({priority}\d+)\-({event_code}\d+)""",
    """%ASA\-\d+\-\d+:\s*({command_module}.*?):\s*Runt\s*({protocol}\w+)\s*({event_name}.*?)\s*\d+""",
    """from\s*(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?)):({src_port}\d+)""",
    """(-|({host}[\w\.-]+))\s*%ASA-|\s+(::ffff:)?({=host}[\w\.-]+)\s*:\s*%ASA-"""
  ]


}
```