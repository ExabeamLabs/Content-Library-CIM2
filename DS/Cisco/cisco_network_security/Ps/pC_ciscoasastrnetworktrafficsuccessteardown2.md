#### Parser Content
```Java
{
Name = "cisco-asa-str-network-traffic-success-teardown-2"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco"
  Product = Cisco Network Security
  TimeFormat = ["MMM dd yyyy HH:mm:ss", "MMM dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [
"""%ASA-"""
"""-30201"""
""": Teardown """
""" duration """
  ]
  Fields = [
    """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
"""\s(({host}[\w.\-]+))\s+([-\s:]+)?%ASA""",
"""({time}\w+ \d\d( \d\d\d\d)? \d\d:\d\d:\d\d+)"""
"""\d\d:\d\d:\d\d\s+(::ffff:)?((?i)system|({host}[\w\.-]+))[\s:]+%ASA-"""
"""%ASA-({priority}\d+)-({event_code}\d+)"""
"""({event_name}Teardown ({protocol}\w+) connection)"""
"""\sconnection\s+({connection_id}\d+)"""
"""\sfor\s+({src_interface}.+?):((::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({src_host}[^\s]+?))\/({src_port}\d+)"""
"""\sto\s+({dest_interface}.+?):((::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({dest_host}[^\s]+?))\/({dest_port}\d+)"""
"""({operation}Teardown ({protocol}\w+) connection)"""
"""\sduration\s+({duration}\S+)\s+bytes\s+({bytes}\d+)(\s+({result_reason}[^\("']+[^\(\s"']))?(\s+\((({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^\)]+?))?)\))?"""
"""%ASA-.*?\((({domain}[^\\\/]+)[\\\/]+)?(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({=domain}[^\)]+?))?)\)"""
  ]


}
```