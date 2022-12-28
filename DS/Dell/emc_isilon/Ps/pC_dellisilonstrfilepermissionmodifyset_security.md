#### Parser Content
```Java
{
Name = dell-isilon-str-file-permission-modify-set_security
  ParserVersion = v1.0.0
  Vendor = Dell
  Product = EMC Isilon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """|SMB|""","""|SET_SECURITY|""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+[\+\-]\d+:\d+)\s+({host}[\w\-.]+)\s+\[[^\]]*\]\s+({user_sid}[^\s\|]+)\|({user_uid}[^\|]*)\|({server_name}[^\|]+)\|({zone_id}[^\|]*)\|({src_ip}[A-Fa-f:\d.]+)\|({protocol}[^\|]*)\|({event_name}SET_SECURITY)\|({result}[^\|\s]*)\|({file_type}[^\|]*)\|({inode}[^\|]*)\|({path}[^\|]*?)\s*$""",
  ]


}
```