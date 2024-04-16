#### Parser Content
```Java
{
Name = "checkpoint-ngfw-cef-network-traffic-access"
  ParserVersion = "v1.0.0"
  Vendor = "Check Point"
  Product = "Check Point NGFW"
  TimeFormat = "epoch"
  Conditions = [
    """|Check Point|VPN-1 & FireWall-1|"""
    """categoryBehavior=/Access"""
  ]
  Fields = [
    """\Wrt=({time}\d{13})"""
    """\Wproto=({protocol}.+?)\s+(\w+=|$)"""
    """\Wact=({action}.+?)\s+(\w+=|$)"""
    """\WdeviceDirection=({direction}\d+)"""
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """\Wspt=({src_port}\d+)"""
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """\Wdpt=({dest_port}\d+)"""
    """\WdestinationServiceName =({service_name}.+?)\s+(\w+=|$)"""
    """\Wdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
    """\Wreason=(?:;|({failure_reason}.+?))\s+(\w+=|$)"""
    """\Wcs1=(?:\s\&|({rule}.+?))\s+(\w+=|$)"""
  ]


}
```