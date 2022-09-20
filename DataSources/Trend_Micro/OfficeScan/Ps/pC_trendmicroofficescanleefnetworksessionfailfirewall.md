#### Parser Content
```Java
{
Name = trendmicro-officescan-leef-network-session-fail-firewall
    Vendor = Trend Micro
    Product = OfficeScan
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """LEEF:""", """|Trend Micro|Deep Security Agent|""", """cat=Firewall""" ]
    Fields = [
      """\Wcat=({alert_type}.+?)\s*(\w+=|$)""",
      """\Wname=({alert_name}.+?)\s*(\w+=|$)""",
      """\Wsev=({alert_severity}\d+)""",
      """\Wdvchost=({host}.+?)\s*(\w+=|$)""",
      """\Wact=({action}.+?)\s*(\w+=|$)""",
      """\WdstMAC=({dest_mac}.+?)\s*(\w+=|$)""",
      """\WsrcMAC=({src_mac}.+?)\s*(\w+=|$)""",
      """\Wsrc=({src_ip}[A-Fa-f:\d.]+)""",
      """\Wdst=({dest_ip}[A-Fa-f:\d.]+)""",
      """\Wproto=({protocol}.+?)\s*(\w+=|$)""",
      """\WsrcPort=({src_port}\d+)""",
      """\WdstPort=({dest_port}\d+)""",
      """\Win=({bytes_in}\d+)""",
      """\Wout=({bytes_out}\d+)""",
    ]
    DupFields = [ "alert_name->event_name" ]
    ParserVersion = "v1.0.0"
  

}
```