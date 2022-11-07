#### Parser Content
```Java
{
Name = juniper-srx-kv-network-session-netscreen
  Vendor = Juniper Networks
  Product = Juniper SRX
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """: NetScreen """, """ [Root]""", """ duration=""", """ src zone=""" ]
  Fields = [
    """\sdevice_id=({host}.+?)\s+\[Root\]""",
    """\[Root\]({event_name}[^:]+?)\-\d+[^\-:]*?:""",
    """\sstart_time="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""",
    """\sduration=({duration}\d+)""",
    """\sservice=({protocol}\w+)""",
    """\ssrc zone=({src_zone}[^\s]+)""",
    """\sdst zone=({dest_zone}[^\s]+)""",
    """\ssent=({bytes_out}\d+)""",
    """\srcvd=({bytes_in}\d+)""",
    """\ssrc=({src_ip}[a-fA-F\d.:]+)""",
    """\sdst=({dest_ip}[a-fA-F\d.:]+)""",
    """\ssrc_port=({src_port}\d+)""",
    """\sdst_port=({dest_port}\d+)""",
    """\ssrc-xlated ip=({src_translated_ip}[a-fA-F\d.:]+)""",
    """\sdst-xlated ip=({dest_translated_ip}[a-fA-F\d.:]+)""",
    """\ssession_id=({session_id}\d+)""",
    """\sreason=({result}.+?)\s*$""",
  ]
  ParserVersion = "v1.0.0"


}
```