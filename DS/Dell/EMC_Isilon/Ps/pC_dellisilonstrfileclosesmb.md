#### Parser Content
```Java
{
Name = dell-isilon-str-file-close-smb
  ParserVersion = v1.0.0
  Vendor = Dell
  Product = EMC Isilon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """|SMB|""","""|CLOSE|""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+(Z|[\+\-]\d+:\d+))""",
     """\d+-\d+-\d+T\d+:\d+:\d+(Z|\+\d+:\d+)?\s*({host}[\w\-.]+)\s+[^\]]*\]:?\s*({user_sid}[^\s\|]+)\|({user_uid}[^\|]*)\|({server_name}[^\|]+)\|({zone_id}[^\|]*)\|({src_ip}[A-Fa-f:\d.]+)\|({protocol}[^\|]*)\|({event_name}CLOSE)\|({result}[^\|\s]*)\|({file_type}[^\|]*)\|({bytes_out}\d+):(\d+)\|({bytes_in}\d+):(\d+)\|({inode}[^\|]*)\|({path}[^\|]*?)\s*$"""#dl fields removed
  ]


}
```