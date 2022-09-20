#### Parser Content
```Java
{
Name = cisco-pix-str-network-start-success-302020
  ParserVersion = "v1.0.0"
  Vendor = Cisco
  Product = Cisco PIX
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%PIX""" , """-302020""", """ ICMP connection for ""","""Built""" ]
  Fields = [
   """({time}\w+\s\d+\s\d+\s\d+:\d+:\d+)\s+({host}[^\s]{1,2000})""",
   """%PIX-({priority}\d+)-({event_code}\d+)""",
   """({event_name}Built ({direction}inbound|outbound) ({protocol}ICMP) connection)"""
   """Built outbound ICMP.*?faddr\s+({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\/({dest_port}\d+))?""",
   """Built inbound ICMP.*?faddr\s+({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\/({src_port}\d+))?""",
   """Built outbound ICMP.*?laddr\s+({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\/(({src_port}\d+))?""",
   """Built inbound ICMP.*?laddr\s+({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\/(({dest_port}\d+))?""",
   ]


}
```