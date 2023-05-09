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
    """({time}\d+-\d+-\d+T\d+:\d+:\d+(([\+\-]\d+:\d+)|Z))\s+({host}[\w\-.]+)\s+([^\[\s]*)?\[[^\]]*\]:?\s+({user_sid}[^\s\|]+)\|({user_uid}[^\|]*)\|({server_name}[^\|]+)\|({zone_id}[^\|]*)\|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\|({protocol}[^\|]*)\|({access}DELETE)\|({result}[^\|\s]*)\|({file_type}[^\|]*)\|({inode}[^\|]*)\|(|({file_path}({file_dir}[^"\|]*?)[\\\/]*({file_name}[^\\\/"\|]+?(\.({file_ext}[^\\\.\s"\|\/]+))?)))\s*""",
    """"fileName"*:"*({file_path}(({file_dir}[^"]+)[\\\/]+)?(({file_name}[^"\\\/]+?(\.({file_ext}[^\."]+))?)))"*,""",
    """\|(FILE|DIR)\|.*?\|({file_path}({file_dir}[^"]+[\\\/]+)?(({file_name}[^"]+?(\.({file_ext}[^\s"]+)))))(\s|")*"""
  ]


}
```