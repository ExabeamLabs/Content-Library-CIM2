#### Parser Content
```Java
{
Name = vmware-nsxfw-cef-network-traffic-success-nsxfw
  ParserVersion = v1.0.0
  Vendor = VMware
  Product = NSX Distributed Firewall
  TimeFormat = "epoch"
  Conditions = [ """CEF:""" ,"""|VMware|NSX FW|""", """destinationZoneURI="""]
  Fields = [
    """\srt=({time}\d{13})"""
    """NSX FW\|[^\|]*\|({action}[^\|]+)"""
    """categoryOutcome=\/({result}[^\s]*)""",
    """eventId=({event_code}[^\s]+)""",
    """proto=({protocol}[^\s]+)""",
    """cs1=({additional_info}[^\s]+)""",
    """cs2=({host}[^\s]+)""",
    """src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """spt=({src_port}\d+)""",
    """dst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """dpt=({dest_port}\d+)"""
    """categoryBehavior=\/({operation}[^\s]+)""",
    """dtz=({dest_country}[^\s]+)"""
  ]


}
```