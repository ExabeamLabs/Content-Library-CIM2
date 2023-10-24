#### Parser Content
```Java
{
Name = "tanium-cp-kv-dns-response-success-tanium"
Vendor = "Tanium"
Product = "Tanium Core Platform"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSZ"
Conditions = [
""" Tanium """
""" Time-(UTC)="2"""
]
Fields = [
"""({host}[\w.\-]+)\s+Tanium """
"""\sEndpoint-Name =\"(-|({src_host}[\w.\-]+))\""""
"""\sTime-\(UTC\)=\"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d)"""
"""\sUsername=\"(-|({user}[\w\.\-]{1,40}\$?))\""""
"""\sQuery=\"(-|({dns_query}[^\"]+))\""""
"""\sOperation=\"(-|({operation}[^\"]+))\""""
"""\sProcess-Name =\"(-|({process_path}({process_dir}[^\"]*?[\\\/]+)?({process_name}[^\"\\\/]+)))\""""
"""\sResponse=\"(\[unresolved\]|(::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\""""
]
ParserVersion = "v1.0.0"


}
```