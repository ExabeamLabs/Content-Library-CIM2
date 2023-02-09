#### Parser Content
```Java
{
Name = unix-dhcpd-str-app-notification-balancedpool
  ParserVersion = v1.0.0
  Conditions = [ """dhcpd:""", """balanced pool""" ]
  Fields = ${DHCPDParsersTemplates.dhcpd-events.Fields}[
    """dhcpd:\s+({event_name}\S+\spool)\s*\w+\s*(\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\/(\d+)\s+({additional_info}.*?)"*\s*$""", #dl fields are removed
  ]

dhcpd-events = {
  Vendor = Unix
  Product = Unix dhcpd
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """\w{3} \d{1,2} \d\d:\d\d:\d\d (::ffff:)?({host}[\w.\-]+) dhcpd:""",
    """dhcpd:\s*({event_name}\S+)""",
  
}
```