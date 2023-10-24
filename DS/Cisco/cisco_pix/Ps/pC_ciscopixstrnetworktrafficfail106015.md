#### Parser Content
```Java
{
Name = cisco-pix-str-network-traffic-fail-106015
  ParserVersion = "v1.0.0"
  Vendor = Cisco
  Product = Cisco PIX
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%PIX""" , """-106015""", """Deny TCP"""]
  Fields = [
   """({time}\w+\s\d+\s\d+\s\d+:\d+:\d+)\s+({host}[^\s]+)""",
   """%PIX-({priority}\d+)-({event_code}\d+)""",
   """({event_name}Deny TCP \(({result_reason}[^\)]*)\))""",
   """\sfrom\s+(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))\/({src_port}\d+)""",
   """\sto\s+(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))\/({dest_port}\d+)""",
   """\sflags\s+(.+?)\s+on interface\s+({interface}\S+)""",# flags is removed
   """({action}Deny)\s({protocol}[^\s]+)"""
   ]


}
```