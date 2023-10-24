#### Parser Content
```Java
{
Name = "dell-emcisilon-str-file-write-success-write"
Vendor = "Dell"
Product = "EMC Isilon"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""|SMB|"""
"""|WRITE|"""
]
Fields = [
"""({time}\d+-\d+-\d+T\d+:\d+:\d+[\+\-]\d+:\d+)\s+({host}[\w\-.]+)\s+\[[^\]]*\]\s+({user_sid}[^\s\|]+)\|({user_uid}[^\|]*)\|({server_name}[^\|]+)\|({zone_id}[^\|]*)\|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\|({protocol}[^\|]*)\|({access}WRITE)\|({result}[^\|\s]*)\|({file_type}[^\|]*)\|({inode}[^\|]*)\|(|({src_file_path}({file_dir}[^"\|]*?)[\\\/]*({src_file_name}[^\\\/"\|]+?(\.({src_file_ext}[^\\\.\s"\|]+))?)))\s+$"""
""""fileName"*:"*({src_file_path}(({file_dir}[^"]+)[\\\/]+)?(({src_file_name}[^"\\\/]+?(\.({src_file_ext}[^\."]+))?)))"*,"""
]
ParserVersion = "v1.0.0"


}
```