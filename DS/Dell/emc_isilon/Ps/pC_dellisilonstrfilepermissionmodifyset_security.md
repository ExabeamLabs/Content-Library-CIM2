#### Parser Content
```Java
{
Name = dell-isilon-str-file-permission-modify-set_security
  ParserVersion = v1.0.0
  Vendor = Dell
  Product = EMC Isilon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """|SMB|""","""|SET_SECURITY|""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+[\+\-]\d+:\d+)\s+({host}[\w\-.]+)\s+\[[^\]]*\]\s+({user_sid}[^\s\|]+)\|({user_uid}[^\|]*)\|({server_name}[^\|]+)\|({zone_id}[^\|]*)\|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\|({protocol}[^\|]*)\|({event_name}SET_SECURITY)\|({result}[^\|\s]*)\|({file_type}[^\|]*)\|({inode}[^\|]*)\|({path}[^\|]*?)\s*$""",
  ]


}
```