#### Parser Content
```Java
{
Name = pan-ngfw-cef-http-session-url-1
  Vendor = "Palo Alto Networks"
  Product = "Prisma Cloud"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "MMM dd yyyy HH:mm:ss"]
  Conditions = [ """CEF:""", """|Palo Alto Networks|LF|""", """|THREAT|url|""" ]
  Fields = [
    """\srt=({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)\s""",
    """\sdvchost=({host}[\w\-\.]+)""",
    """({event_category}THREAT)""",
    """\sact=({action}[^\s]+)""",
    """\sproto=({protocol}[^\s]+)""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """\ssuser=(|({email_address}[^@\s=]+@[^\s=\.]+\.[^\s=]+)|(({domain}[^\s=\\]+)[\\]{1,20})?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s\w+=""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s{1,100}\w+=""",
    """\sdpt=({dest_port}\d+)""",
    """\sspt=({src_port}\d+)""",
    """\scs2=({category}[^=]+?)\scs2Label=URLCategory""",
    """\srequestContext=(|({mime}[^=]+))\s{1,100}\w+=""",
    """\srequest="?({url}(\w+\\{0,20}:\/{1,20})?({web_domain}[^\/:"\s]+)?({uri_path}\/[^\?\s"]*)?({uri_query}\?[^\s"]+)?)"?\s\w+=""",
    """\sflexString2=({direction}[^=]+?)\s\w+=""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
    """\scs4=({src_network_zone}[^\s]+)""",
    """\scs5=({dest_network_zone}[^\s]+)""",
    """deviceInboundInterface=({src_interface}[^\s]+)""",
    """deviceOutboundInterface=({dest_interface}[^\s]+)""",
    """deviceExternalId=({serial_num}\d+)""",
    """\sapp=(not-applicable|({network_app}[^=]+?))\s\w+="""
	  """sourceTranslatedAddress=({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s""",
    """destinationTranslatedAddress=({dest_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s"""
    """\sdvchost=({device_name}[\w\-\.]+)""",
  ]
  ParserVersion = v1.0.0


}
```