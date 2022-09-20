#### Parser Content
```Java
{
Name = cisco-pix-str-network-session-fail-302014
  ParserVersion = "v1.0.0"
  Vendor = Cisco
  Product = Cisco PIX
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%PIX""" , """-302014""", """Teardown TCP connection"""]
  Fields = [
   """({time}\w+\s\d+\s\d+\s\d+:\d+:\d+)\s+({host}[^\s]+)""",
   """%PIX-({priority}\d+)-({event_code}\d+)""",
   """({event_name}({action}Teardown)\s+({protocol}[^\s]+))""",
   """for.+?:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\/({src_port}\d+))""",
   """to.+?:({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\/({dest_port}\d+))?""",
 ]


}
```