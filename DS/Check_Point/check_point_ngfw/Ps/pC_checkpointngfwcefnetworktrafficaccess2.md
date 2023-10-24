#### Parser Content
```Java
{
Name = "checkpoint-ngfw-cef-network-traffic-access-2"
  ParserVersion = "v1.0.0"
  Vendor = "Check Point"
  Product = "Check Point NGFW"
  TimeFormat = "epoch"
  Conditions = [
    """|Check Point|VPN-1|"""
    """/Access"""
  ]
  Fields = [
    """\srt=({time}\d{13})"""
    """dpt=({dest_port}\d+)"""
    """spt=({src_port}\d+)"""
    """cs2=({rule}.+?)\slayer"""
    """rule_action=({action}[^\s]+)\s"""
    """direction=({direction}[^\s]+)\s"""
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s"""
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s"""
    """proto=({protocol}[^\s]+)\s"""
    """originsicname=CN\\=({host}[^\s,;\\]+)"""
    """act=({action}.+?)\s\w+="""
    """categoryOutcome=(\/)?({result}.+?)\s\w+="""
    """originsicname=CN\\=({host}[^\s,;\\]+)"""
    """act=({action}.+?)\s\w+="""
    """categoryOutcome=(\/)?({result}.+?)\s\w+="""
  ]


}
```