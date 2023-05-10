#### Parser Content
```Java
{
Name = dell-emcisilon-str-file-read-success-open
  ParserVersion = v1.0.0
  Vendor = Dell
  Product = EMC Isilon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """|SMB|""","""|OPEN|""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+(([\+\-]\d+:\d+)|Z))\s+({host}[\w\-.]+)\s+([^\[\s]*)?\[[^\]]*\]:?\s+({user_sid}[^\s\|]+)\|({user_uid}[^\|]*)\|({server_name}[^\|]+)\|({zone_id}[^\|]*)\|({src_ip}[A-Fa-f:\d.]+)\|({protocol}[^\|]*)\|({access}OPEN)\|({result}[^\|\s]*)\|({desire_access}[^\|]*)\|({file_type}[^\|]*)\|({create_result}[^\|]*)\|(|({inode}[^\|]*))\|({file_path}({file_dir}[^"]+[\\\/])?({file_name}[^"]+(\.({file_ext}[^"]+)?)\s+)?)""",
  ]


}
```