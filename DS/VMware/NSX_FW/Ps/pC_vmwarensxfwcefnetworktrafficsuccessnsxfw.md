#### Parser Content
```Java
{
Name = vmware-nsxfw-cef-network-traffic-success-nsxfw
  ParserVersion = v1.0.0
  Vendor = VMware
  Product = NSX FW
  TimeFormat = "epoch"
  Conditions = [ """CEF:""" ,"""|VMware|NSX FW|""", """destinationZoneURI="""]
  Fields = [
    """rt=({time}\d+)"""
    """NSX FW\|[^\|]*\|({action}[^\|]+)"""
    """categoryOutcome=\/({result}[^\s]*)""",
    """eventId=({event_code}[^\s]+)""",
    """proto=({protocol}[^\s]+)""",
    """cs1=({additional_info}[^\s]+)""",
    """cs2=({host}[^\s]+)""",
    """src=({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})""",
    """spt=({src_port}\d+)""",
    """dst=({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})""",
    """dpt=({dest_port}\d+)"""
    """categoryBehavior=\/({operation}[^\s]+)""",
    """dtz=({dest_country}[^\s]+)"""
  ]


}
```