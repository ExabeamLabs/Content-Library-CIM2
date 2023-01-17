#### Parser Content
```Java
{
Name = fortinet-fortigate-cef-http-session-webfilter
  Vendor = Fortinet
  Product = FortiGate
  TimeFormat = "epoch"
  Conditions = [ """|Fortinet|Fortigate|""", """|utm:webfilter """, """FTNTFGTlevel=""", """FTNTFGTsubtype=webfilter""" ]
  Fields = [
    """FTNTFGTeventtime=({time}\d{13})""",
    """\s\d\d:\d\d:\d\d\s({host}[\w\-\.]+)""",
    """\|Fortinet\|Fortigate\|([^|]+\|){2}({event_name}[^|]+)\|""",
    """\ssrc=({src_ip}[a-fA-F\d\.]+)""",
    """\sspt=({src_port}\d{1,5})""",     
    """\sdhost=({web_domain}[^\s]+?)\s\w+=""", 
    """\sdst=({dest_ip}[a-fA-F\d\.]+)""",
    """\sdpt=({dest_port}\d{1,5})""",
    """\sact=({action}[^=]+?)\s\w+=""",
    """\sproto=({protocol}[^\s]+)"""
    """\srequest=({url}(\w{1,5}:\/\/)?[^\s\/\?]+({uri_path}\/[^\s\?]*)?(\?({uri_query}[^\s]*)))\s\w+=""",
    """\sout=({bytes_out}\d+)""",
    """\sin=({bytes_in}\d+)""",
    """deviceDirection=({direction}\d)""",
    """\smsg=({additional_info}[^=]+?)\s\w+="""
  ]
  ParserVersion = "v1.0.0"


}
```