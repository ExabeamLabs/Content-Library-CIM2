#### Parser Content
```Java
{
Name = pan-wildfire-leef-alert-trigger-success-wildfire
  Conditions = [ """|Palo Alto Networks|PAN-OS""", """|Subtype=wildfire""" ]
  ParserVersion = "v1.0.0"

leef-pan-alert = {
  Vendor = Palo Alto Networks
  Product = Palo Alto WildFire
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Fields = [
    """ReceiveTime=({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)""",
    """({host}[\w\.-]+)(\s+|,"+)LEEF:""",
    """\|DeviceName =({host}[^\|"]+?)\s*(\||"*$)""",
    """\|Subtype=({alert_type}[^\|]+)""",
    """\|src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\|dst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\|Application=({process_name}[^\|]+)""",
    """\|srcPort=({src_port}\d+)""",
    """\|dstPort=({dest_port}\d+)""",
    """\|proto=({protocol}[^\|]+)""",
    """\|action=({result}[^\|]+)""",
    """\|Miscellaneous="({additional_info}[^"\|]+)"""",
    """\|ThreatID=({alert_name}[^\|]+)""",
    """\|URLCategory=({category}[^\|]+)""",
    """\|Severity=({alert_severity}[^\|]+)""",
    """\|ThreatCategory=(?:unknown|({threat_category}[^\|]+))""",
    """usrName =({domain}[^\\\|]+)\\({user}[^\s\|]+)""",
    """\|SourceZone=({src_network_zone}[^\|]+?)\|""",
    """\|DestinationZone=({dest_network_zone}[^\|]+?)\|""",
    
}
```