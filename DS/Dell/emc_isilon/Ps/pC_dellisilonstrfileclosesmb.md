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
     """\d+-\d+-\d+T\d+:\d+:\d+(Z|\+\d+:\d+)?\s*({host}[\w\-.]+)\s+[^\]]*\]:?\s*({user_sid}[^\s\|]+)\|({user_uid}[^\|]*)\|({src_zone}[^\|]+)\|({zone_id}[^\|]*)\|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\|({protocol}[^\|]*)\|({event_name}CLOSE)\|({result}[^\|\s]*)\|({file_type}[^\|]*)\|({bytes_out}\d+):(\d+)\|({bytes_in}\d+):(\d+)\|({inode}[^\|]*)\|({path}[^\|]*?)\s*$"""#dl fields removed
  ]


}
```