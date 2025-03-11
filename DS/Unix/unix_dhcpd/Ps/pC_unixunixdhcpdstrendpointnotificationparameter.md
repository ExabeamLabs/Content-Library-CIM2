#### Parser Content
```Java
{
Name = unix-unixdhcpd-str-endpoint-notification-parameter
  ParserVersion = "v1.0.0"
  Conditions = [ """dhcpd:""", """Detected host has parameter""" ]
  Fields = ${DHCPDParserTemplates.dhcpd-events-2.Fields}[
    """dhcpd:\s*({event_name}\S+)\s({additional_info}.+)""",
  ]

dhcpd-events-2 = {
  Vendor = Unix
  Product = Unix dhcpd
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """\w{3} \d+ \d\d:\d\d:\d\d (::ffff:)?({host}[\w.\-]+) dhcpd:""",
    """dhcpd:\s*({event_name}\S+)""",
  
}
```