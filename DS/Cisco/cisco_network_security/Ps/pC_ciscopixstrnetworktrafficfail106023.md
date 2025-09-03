#### Parser Content
```Java
{
Name = cisco-pix-str-network-traffic-fail-106023
  ParserVersion = "v1.0.0"
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%PIX""" , """-106023""", """Deny """,""" by access-group""" ]
  Fields = [
        """({time}\w+\s+\d+\s+\d+\s+\d+:\d+:\d+)\s+({host}[^\s]+)""",
        """%PIX-({priority}\d+)-({event_code}\d+)""",
        """\ssrc\s+({src_interface}[^:]+):({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\/({src_port}\d+))?""",
        """({event_name}({result}Deny)\s+({protocol}\w+))"""
        """dst.+?:({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\/({dest_port}\d+))?""",
        """ by access-group(\s+"+({access_group}[^\s"]+))?"""
 ]


}
```