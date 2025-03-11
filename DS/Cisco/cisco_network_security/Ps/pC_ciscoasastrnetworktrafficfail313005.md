#### Parser Content
```Java
{
Name = cisco-asa-str-network-traffic-fail-313005
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = ["MMM dd yyyy HH:mm:ss", "MMM dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ """-313005""", """%ASA-""", """error message:""" ]
  Fields = [
    """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
"""\s(({host}[\w.\-]+))\s+([-\s:]+)?%ASA""",
    """\s(::ffff:)?(-({host}[\w\.-]+))[\s:]+%ASA-""",
    """({time}\w+ \d+ \d{0,4}\s*\d\d:\d\d:\d\d)""",
    """%ASA-({priority}\d+)-({event_code}\d+):\s*({event_name}.*?)\sfor\s*({protocol}\w+)\s""",
    """\ssrc\s*({src_interface}\w+):((::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({src_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({src_host}[^\s]+?))((\(({domain}[^\\]+)\\({email_address}[^@]+@[^.]+\.[^)]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)\))?\))?""",
    """\sdst\s*({dest_interface}\w+):((::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({dest_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({dest_host}[^\s]+?)(\s|$))""",
    """%ASA.*?:\s*({failure_reason}[^:]+)\s*error\s*"""
    """\ssrc\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\/({src_port}\d+))?"""
   """\sdst\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\/({dest_port}\d+))?"""
  ]



}
```