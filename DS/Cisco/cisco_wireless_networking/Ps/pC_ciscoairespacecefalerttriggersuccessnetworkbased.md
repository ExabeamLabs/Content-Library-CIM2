#### Parser Content
```Java
{
Name = cisco-airespace-cef-alert-trigger-success-networkbased
  Vendor = Cisco
  Product =  Cisco Wireless Networking
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """CEF:""" , """|Cisco|Airespace|""", """dvchost=""", """catdt=Network-based IDS"""  ]
  Fields = [
    """dvchost=({host}[^=]+?)\s+\w+=""",
    """({alert_type}Airespace)""",
    """\|Cisco\|([^\|]*\|){3}({alert_name}[^\|]+)\|(Unknown|({alert_severity}[^\|]+))""",
    """\|Cisco\|([^\|]*\|){2}(({alert_type}[^\|\d]+)|({event_code}\d+))\s*\|""",
    """eventId=({alert_id}\d+)""",
    """src=(0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """categoryOutcome=(\/)?({result}[^=]+?)\s+\w+=""",
    """categorySignificance=(\/)?({category_significance}[^=\/]+?)\s+\w+=""",
    """categoryBehavior=(\/)?({category_behavior}[^=]+?)\s+\w+=""",
    """smac=({src_mac}[^=]+?)\s+\w+=""",
    """dmac=({dest_mac}[^=]+?)\s+\w+=""",
    """dvc=({host_ip}[a-fA-F:\d.]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```