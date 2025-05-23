#### Parser Content
```Java
{
Name = pan-ngfw-cef-alert-trigger-success-spyware
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = "MMM dd yyyy HH:mm:ss zzz"
  Conditions = [ """CEF""", """|Palo Alto Networks|PAN-OS|""", """|THREAT|""", """cat=spyware"""  ]
  Fields = [
    """\sdvchost=({host}[\w\-.]+)""",
    """\|rt=({time}\w\w\w\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d \w\w\w)""",
    """({alert_type}spyware)""",
    """\scat=({alert_name}[^=]+)\s+(\w+=|$)""",
    """Palo Alto Networks\|PAN-OS\|[^\|]+\|({alert_name}[^(:]+)(\s*[^\|]+)\|""",
    """Palo Alto Networks\|PAN-OS\|([^\|]+\|){3}({alert_severity}\d)\|rt=""",
    """\sshost=({src_host}[^=]+)\s+(\w+=|$)""",
    """\sdhost=({dest_host}[^=]+)\s+(\w+=|$)""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+(\w+=|$)""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+(\w+=|$)""",
    """\seventId=({alert_id}\d+)\s+(\w+=|$)""",
    """\sapp=({threat_category}[^=]+)\s+(\w+=|$)""",
    """\sproto=({protocol}[^=]+?)\s+\w+=""",
    """\sact=({action}[^=]+?)\s+\w+=""",
    """\sspt=({src_port}\d+)""",
    """\sdpt=({dest_port}\d+)""",
    """\scs1="*({rule}[^="]+?)"*\s+\w+="""
    """\sapp=({app}[^=]+)\s+\w+=""",
    """\scs2=({category}[^=]+)\s+\w+=""",
    """\sflexString2=({direction}[^=]+)\s+\w+="""
    """\scs4=({src_network_zone}[^\s]+)"""
    """\scs5=({dest_network_zone}[^\s]+)"""
    """deviceInboundInterface=({src_interface}[^\s]+)"""
    """deviceOutboundInterface=({dest_interface}[^\s]+)"""
    """deviceExternalId=({serial_num}\d+)"""
    """\sapp=(not-applicable|({network_app}[^=]+?))\s\w+="""
	  """sourceTranslatedAddress=({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s"""
    """destinationTranslatedAddress=({dest_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s"""
  ]
  DupFields = ["host->device_name"]
  ParserVersion = v1.0.0


}
```