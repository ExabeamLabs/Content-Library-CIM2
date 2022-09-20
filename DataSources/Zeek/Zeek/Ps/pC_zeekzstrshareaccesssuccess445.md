#### Parser Content
```Java
{
Name = zeek-z-str-share-access-success-445
  ParserVersion = v1.0.0
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "epoch_sec"
  Conditions = [ """ SMB::FILE_OPEN """, """ 445 """ ]
  Fields = [
     """({time}\d{10})\.\d{6}\s+({connection_id}[^\s]+)\s+(?:-|(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+))\s+(?:-|(({src_port}\d+?)|[^\s]+))\s+(?:-|(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+))\s+(?:-|(({dest_port}\d+?)|[^\s]+))\s+(?:-|({file_id}[^\s]+))\s+(?:-|({event_name}[^\s]+))\s+(?:-|({share_path}[^\s]+))\s+(?:-|({file_name}[^\s]+))\s+(?:-|({bytes}\d+)?)\s+(?:-|({src_file_name}[^\s]+))\s+(?:-|({times_modified}[^\s]+))\s+(?:-|({time_accessed}[^\s]+))\s+(?:-|({time_created}[^\s]+))\s+(?:-|({time_changed}[^\s]+?))\s*""",
     """SMB::({access}FILE_OPEN)""",
     """\d{10}\.\d{6}\t([^\s]+\s+){8}({file_path}({file_dir}[^\st]*?(\\u005c|[\\\/])*)({file_name}[^\s\\\/]+?(\.({file_ext}[^\s\\\/\.]+))?))\s""",
     """({protocol}SMB)"""
    ]


}
```