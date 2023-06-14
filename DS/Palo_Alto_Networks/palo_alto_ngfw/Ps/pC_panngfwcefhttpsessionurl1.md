#### Parser Content
```Java
{
Name = pan-ngfw-cef-http-session-url-1
  Vendor = "Palo Alto Networks"
  Product = "Palo Alto NGFW"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """CEF:""", """|Palo Alto Networks|LF|""", """|THREAT|url|""" ]
  Fields = [
    """\srt=({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)\s""",
    """\sdvchost=({host}[\w\-\.]+)""",
    """({event_category}THREAT)""",
    """\sact=({action}[^\s]+)""",
    """\sproto=({protocol}[^\s]+)""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """\ssuser=(|({email_address}[^@\s=]+@[^\s=\.]+\.[^\s=]+)|(({domain}[^\s=\\]+)[\\]{1,20})?({user}[^\s=]+?))\s\w+=""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s{1,100}\w+=""",
    """\sdpt=({dest_port}\d+)""",
    """\sspt=({src_port}\d+)""",
    """\scs2=({category}[^=]+?)\scs2Label=URLCategory""",
    """\srequestContext=(|({mime}[^=]+))\s{1,100}\w+=""",
    """\srequest="?({url}(\w+\\{0,20}:\/{1,20})?({web_domain}[^\/:"\s]+)?({uri_path}\/[^\?\s"]*)?({uri_query}\?[^\s"]+)?)"?\s\w+=""",
    """\sflexString2=({direction}[^=]+?)\s\w+=""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
  ]
  ParserVersion = v1.0.0


}
```