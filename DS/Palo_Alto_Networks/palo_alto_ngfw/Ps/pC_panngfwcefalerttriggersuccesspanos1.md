#### Parser Content
```Java
{
Name = pan-ngfw-cef-alert-trigger-success-panos-1
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = ["MMM dd yyyy HH:mm:ss zzz","MMM dd yyyy HH:mm:ss"]
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|Palo Alto Networks|""", """|THREAT|""", """PanOSThreatCategory="""  ]
  Fields = [
    """\s({host}[\w\-.]+?)\sCEF:""",
    """\sdvchost=({host}[\w\-.]+)""",
    """\sdvchost=({device_name}[\w\-.]+)""",
    """\srt=({time}\w\w\w\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)"""
    """\|rt=({time}\w\w\w\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d \w\w\w)""",
    """({alert_type}THREAT)""",
    """\scat=({alert_name}[^=]+)\s+\w+=""",
    """\|({alert_name}[^\|]+)\|THREAT\|({alert_severity}\d+)\|""",
    """\|THREAT\|(virus|spyware|vulnerability|wildfire-virus)\|({alert_severity}\d+)\|""", 
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+\w+=""",	
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+\w+=""",
    """\sapp=({app}[^=]+)\s+\w+=""",
    """\sproto=({protocol}[^=]+?)\s+\w+=""",
    """\sact=({action}[^=]+?)\s+\w+=""",
    """\sspt=({src_port}\d+)""",
    """\sdpt=({dest_port}\d+)""",
    """\scs1="*({rule}[^="]+?)"*\s+\w+=""",
    """PanOSThreatCategory=({threat_category}[^=]+?)\s+\w+=""",
    """suser=((({domain}[^\\=]+?)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))\s+\w+=""",
    """\scs2=({category}[^=]+)\s+\w+=""",
    """\sflexString2=({direction}[^=]+)\s+\w+=""",
    """\scs4=({src_network_zone}[^\s]+)""",
    """\scs5=({dest_network_zone}[^\s]+)""",
    """deviceInboundInterface=({src_interface}[^\s]+)""",
    """deviceOutboundInterface=({dest_interface}[^\s]+)""",
    """deviceExternalId=({serial_num}\d+)""",
    """\sapp=(not-applicable|({network_app}[^=]+?))\s\w+="""
	  """sourceTranslatedAddress=({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s""",
    """destinationTranslatedAddress=({dest_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s"""
  ]



}
```