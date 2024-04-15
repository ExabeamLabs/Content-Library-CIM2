#### Parser Content
```Java
{
Name = "tanium-im-kv-file-write-success-write"
Vendor = "Tanium"
Product = "Tanium Integrity Monitor"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""" Tanium """
""" Computer-Name =""""
""" Process-Path=""""
""" File-Path=""""
"""Change-Type="Write""""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+\+?\-?\d\d:\d\d)\s+({host}[^\s]+)\s+Tanium"""
"""\sUser="({user}[^"]+)""""
"""Computer-Name ="({dest_host}[^"]+)""""
"""File-Path="({file_path}({file_dir}[^"]+\\)({file_name}[^"]+\.({file_ext}[^"]+)))"""
"""Process-Path="({process_path}[^"]+(\\|\/)({process_name}[^"]+))""""
"""File-Path="(|({src_file_path}[^=]+?))"\s\w+="""
"""Change-Type="({event_name}Write)""""
]
ParserVersion = "v1.0.0"


}
```