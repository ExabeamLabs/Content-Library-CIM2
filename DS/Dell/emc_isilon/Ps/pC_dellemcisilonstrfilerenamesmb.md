#### Parser Content
```Java
{
Name = dell-emcisilon-str-file-rename-smb
  Vendor = Dell
  Product = EMC Isilon
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """|SMB|""","""|RENAME|""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+[\+\-]\d+:\d+)\s+({host}[\w\-.]+)\s+\[[^\]]*\]\s+({user_sid}[^\s\|]+)\|({user_uid}[^\|]*)\|({server_name}[^\|]+)\|({zone_id}[^\|]*)\|({src_ip}[A-Fa-f:\d.]+)\|({protocol}[^\|]*)\|({event_name}RENAME)\|({result}[^\|\s]*)\|({file_type}[^\|]*)\|({inode}[^\|]*)\|([^\|]*?)\|({dest_path}[^\|]*?)\s*$""",#dl field removed
  ]


}
```