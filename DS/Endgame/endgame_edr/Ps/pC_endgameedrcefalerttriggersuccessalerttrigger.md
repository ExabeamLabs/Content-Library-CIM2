#### Parser Content
```Java
{
Name = endgame-edr-cef-alert-trigger-success-alerttrigger
  ParserVersion = v1.0.0
  Vendor = Endgame 
  Product = Endgame EDR
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Endgame|""", """EventResponse|""" ]
  Fields = [
    """\s({host}[\w\-.]+)\s+CEF:""",
    """CEF:([^\|]*\|){4}({alert_name}[^\|]+)""",
    """CEF:([^\|]*\|){5}({alert_type}[^\|]+)""",
    """CEF:([^\|]*\|){6}({alert_severity}[^\|]+)""",
    """\Wdvc=({host}[A-Fa-f:\d.]+)""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\Wrt=({time}\d{13})""",
    """\Wcfp1=({malware_score}.+?)\s+(\w+=|$)""",
    """\Wcs1=({sensor_id}.+?)\s+(\w+=|$)""",
    """\Wcs2=({malware_url}.+?)\s+(\w+=|$)""",
# endgame_alert_type is removed
    """\Wdhost=({dest_host}[\w\-.]+)\s+(\w+=|$)""",
    """\WexternalId=({alert_id}.+?)\s+(\w+=|$)""",
    """\WfileHash=({hash_md5}.+?)\s+(\w+=|$)""",
    """\WfilePath=(|({process_path}({process_dir}[^"]*?)[\\\/]*({process_name}[^\\\/"]+?)))\s+(\w+=|$)""",
    """\Wfname=({process_name}.+?)\s+(\w+=|$)""",
    """\Wfsize=({bytes}\d+)\s+(\w+=|$)""",
    """\Wmsg=({event_name}.+?)\s+(\w+=|$)""",
  ]


}
```