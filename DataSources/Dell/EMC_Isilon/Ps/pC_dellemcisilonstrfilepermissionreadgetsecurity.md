#### Parser Content
```Java
{
Name = dell-emcisilon-str-file-permission-read-getsecurity
  ParserVersion = v1.0.0
  Vendor = Dell
  Product = EMC Isilon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """|SMB|""","""|GET_SECURITY|""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+[\+\-]\d+:\d+)\s+({host}[\w\-.]+)\s+\[[^\]]*\]\s+({user_sid}[^\s\|]+)\|({user_uid}[^\|]*)\|({server_name}[^\|]+)\|({zone_id}[^\|]*)\|({src_ip}[A-Fa-f:\d.]+)\|({protocol}[^\|]*)\|({event_name}GET_SECURITY)\|({result}[^\|\s]*)\|({file_type}[^\|]*)\|({inode}[^\|]*)\|({path}[^"]+)\/({file_name}[^"]+)(\.({file_ext}[^"]+))?"""",
  ]


}
```