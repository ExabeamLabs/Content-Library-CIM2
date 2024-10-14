#### Parser Content
```Java
{
Name = fortinet-fortigate-cef-dns-queryresponse
  ParserVersion = "v1.0.0"
  Conditions = [ """|Fortinet|Fortigate|""", """FTNTFGTsubtype=dns""" ]

fortinet-network-info = {
  Vendor = Fortinet
  Product = FortiGate
  TimeFormat = "epoch_sec"
  Fields = [
    """FTNTFGTeventtime=({time}\d{10})""",
    """\s\d\d:\d\d:\d\d\s({host}[\w\-\.]+)""",
    """\|Fortinet\|Fortigate\|([^|]+\|){2}({event_name}[^|]+)\|""",
    """\smsg=({additional_info}[^"]+?)\s*(\w+=|$)""",
    """\Wtz="?({tz}[+-]\d+)"""
    """FTNTFGTeventtype=({operation_type}[^=]+?)(\s+\w+=|$)"""
    """FTNTFGTsubtype=({subtype}[^=]+?)(\s+\w+=|$)"""
    """FTNTFGTdstcountry=({dest_country}[^=]+?)(\s+\w+=|$)"""
    """cat=({category}[^=]+?)(\s+\w+=|$)"""
    """FTNTFGTsrccountry=({src_country}[^=]+?)(\s+\w+=|$)"""
    """FTNTFGTdstintfrole=({dest_role}[^=]+?)(\s+\w+=|$)"""
    """FTNTFGTapp=({app}[^=]+?)(\s+\w+=|$)"""
    """dhost=({dest_host}[^=]+?)(\s+\w+=|$)"""
    """msg=({additional_info}[^=]+?)(\s+\w+=|$)"""
    """FTNTFGTdstuser=({user}[^=]+?)(\s+\w+=|$)"""
    """FTNTFGTapprisk=({alert_severity}[^=]+?)(\s+\w+=|$)"""
    """act=({action}[^=]+?)(\s+\w+=|$)"""
    """dpt=({dest_port}\d+)"""
    """spt=({src_port}\d+)"""
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  
}
```