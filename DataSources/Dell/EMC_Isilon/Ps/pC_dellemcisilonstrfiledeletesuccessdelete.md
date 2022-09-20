#### Parser Content
```Java
{
Name = dell-emcisilon-str-file-delete-success-delete
  ParserVersion = v1.0.0
  Vendor = Dell
  Product = EMC Isilon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """|SMB|""","""|DELETE|""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+(([\+\-]\d+:\d+)|Z))\s+({host}[\w\-.]+)\s+([^\[\s]*)?\[[^\]]*\]:?\s+({user_sid}[^\s\|]+)\|({user_uid}[^\|]*)\|({server_name}[^\|]+)\|({zone_id}[^\|]*)\|({src_ip}[A-Fa-f:\d.]+)\|({protocol}[^\|]*)\|({access}DELETE)\|({result}[^\|\s]*)\|({file_type}[^\|]*)\|({inode}[^\|]*)\|(|({src_file_path}({file_dir}[^"\|]*?)[\\\/]*({src_file_name}[^\\\/"\|]+?(\.({src_file_ext}[^\\\.\s"\|\/]+))?)))\s*""",
    """"fileName"*:"*({src_file_path}(({file_dir}[^"]+)[\\\/]+)?(({src_file_name}[^"\\\/]+?(\.({src_file_ext}[^\."]+))?)))"*,"""
  ]


}
```