#### Parser Content
```Java
{
Name = unix-dhcpd-str-dhcp-traffic-dhcpinform
  ParserVersion = v1.0.0
  Conditions = [ """ dhcpd""", """ DHCPINFORM """ ]
  Fields = ${DHCPDParsersTemplates.dhcpd-events.Fields}[
    """({event_name}DHCPINFORM) from ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))? via (({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?:?|({dest_interface}[\w-]+))""",
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