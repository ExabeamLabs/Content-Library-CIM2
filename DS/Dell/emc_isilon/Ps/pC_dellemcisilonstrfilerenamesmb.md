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
    """({time}\d+-\d+-\d+T\d+:\d+:\d+[\+\-]\d+:\d+)\s+({host}[\w\-.]+)\s+\[[^\]]*\]\s+({user_sid}[^\s\|]+)\|({user_uid}[^\|]*)\|({src_zone}[^\|]+)\|({zone_id}[^\|]*)\|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\|({protocol}[^\|]*)\|({event_name}RENAME)\|({result}[^\|\s]*)\|({file_type}[^\|]*)\|({inode}[^\|]*)\|([^\|]*?)\|({dest_path}[^\|]*?)\s*$""",#dl field removed
  ]


}
```