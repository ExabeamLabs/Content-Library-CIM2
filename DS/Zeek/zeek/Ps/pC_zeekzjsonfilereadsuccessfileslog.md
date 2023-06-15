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
    """"tx_hosts\\?"+:\[\\*"*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\\*"*\]""",
    """"rx_hosts\\?"+:\[\\*"*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\\*"*\]""",
    """"conn_uids\\?"+:\[\\*"*({connection_uids}[^\]]+?)\\{0,25}"*\]""",
    """"source\\?"+:\\?"+({protocol}[^"\\]+)""",
    """"analyzers\\?"+:\[({analyzers}.+?)\]""",
    """"mime_type\\?"+:\\?"+({mime}[^"\\]+)""",
    """"filename\\?"+:\\?"+({file_path}({file_dir}[^"]*?(\\u005c|[\\\/])*)({file_name}[^"\\\/]+?(\.({file_ext}[^"\\\/\.]+))?))\s*\\?"""",
    """"seen_bytes\\?"+:({bytes}\d+)""",
    """"total_bytes\\?"+:({bytes}\d+)""",
    """"md5\\?"+:\\?"+({hash_md5}[^"\\]+)""",
    """"sha1\\?"+:\\?"+({hash_sha1}[^"\\]+)"""
  ]


}
```