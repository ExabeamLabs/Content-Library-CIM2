#### Parser Content
```Java
{
Name = threatblockr-t-kv-network-traffic-packatlog
  Vendor = ThreatBlockr
  Product = ThreatBlockr
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """ threatblockr """, """ packet_log """, """, as_name=""", """, as_num=""", """ action=""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)\sthreatblockr""",
    """\ssrc=(({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[\w\-.]+?))(,\s\w+=|\s*$)""",
    """\sdst=(({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-.]+?))(,\s\w+=|\s*$)""",
    """\ssrc_port=({src_port}\d{1,5})""",
    """\sdst_port=({dest_port}\d{1,5})""",
    """\sdirection=({direction}[^=]+?)(,\s\w+=|\s*$)""",
    """\sproto=({protocol}[^=]+?)(,\s\w+=|\s*$)""",
    """\saction=({action}[^=]+?)(,\s\w+=|\s*$)""",
    """\sreason=({additional_info}[^=]+?)(,\s\w+=|\s*$)""",
    """\sgroup="({group_name}[^"]+?)"(,\s\w+=|\s*$)""",
    """\scountry="({country}[^"]+?)"(,\s\w+=|\s*$)""",
    """\s(al|dl)_active="({rule}[^"]+?)"(,\s\w+=|\s*$)"""
  ]
  DupFields = [ "action->result" ]
  ParserVersion = "v1.0.0"


}
```