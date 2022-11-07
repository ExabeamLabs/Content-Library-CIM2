#### Parser Content
```Java
{
Name = zeek-z-json-file-read-success-fileslog
  ParserVersion = v1.0.0
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """/files.log""",""""fuid\":""", """"conn_uids\":""" ]
  Fields = [
    """"HOST"+:\s*"+({host}[^"]+)"""",
    """"TAGS"+:\s*"+({event_code}[^"]+)"""",
    """"ts\\?"+:\\?"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
    """"tx_hosts\\?"+:\[\\*"*({src_ip}[a-fA-F\d.:]+)\\*"*\]""",
    """"rx_hosts\\?"+:\[\\*"*({dest_ip}[a-fA-F\d.:]+)\\*"*\]""",
    """"conn_uids\\?"+:\[\\*"*({connection_uid}[^\]]+?)\\{0,25}"*\]""",
    """"source\\?"+:\\?"+({protocol}[^"\\]+)""",
    """"analyzers\\?"+:\[({analyzers}.+?)\]""",
    """"mime_type\\?"+:\\?"+({mime}[^"\\]+)""",
    """"filename\\?"+:\\?"+({src_file_path}({file_dir}[^"]*?(\\u005c|[\\\/])*)({src_file_name}[^"\\\/]+?(\.({src_file_ext}[^"\\\/\.]+))?))\s*\\?"""",
    """"seen_bytes\\?"+:({bytes}\d+)""",
    """"total_bytes\\?"+:({bytes}\d+)""",
    """"md5\\?"+:\\?"+({hash_md5}[^"\\]+)""",
    """"sha1\\?"+:\\?"+({hash_sha1}[^"\\]+)"""
  ]
  DupFields = [ "src_file_name->file_name" ]


}
```