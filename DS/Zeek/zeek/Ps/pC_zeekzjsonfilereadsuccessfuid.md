#### Parser Content
```Java
{
Name = "zeek-z-json-file-read-success-fuid"
  Vendor = "Zeek"
  Product = "Zeek"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [
   """files","""
   """"fuid":"""
   """"conn_uids":"""
  ]
  Fields = [
    """"_system_name":"({host}[^"]+)""",
    """"ts":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """"tx_hosts":\["({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"\]""",
    """"rx_hosts":\["({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"\]""",
    """"conn_uids":\["({connection_uids}[^"]+)"\]""",
    """"source":"({protocol}[^"]+)""",
    """"analyzers":\[({analyzers}.+?)\]""",
    """"mime_type":"({mime}[^"]+)""",
    """"seen_bytes":"?({bytes}\d+)""",
    """"total_bytes":({bytes}\d+)""",
    """"md5":"({hash_md5}[^"]+)""",
    """"sha1":"({hash_sha1}[^"]+)""",
    """"filename":"({src_file_name}[^"]+?(\.({file_ext}\w+))?)"""",
  ]
  ParserVersion = "v1.0.0"


}
```