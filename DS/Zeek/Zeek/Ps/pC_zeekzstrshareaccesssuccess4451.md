#### Parser Content
```Java
{
Name = zeek-z-str-share-access-success-445-1
  ParserVersion = v1.0.0
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "epoch_sec"
  Conditions = [ """/smb_mapping.log""", """ 445 """ ]
  Fields = [
     """({time}\d{10})\.\d{6}\s+({connection_id}[^\s]+)\s+(?:-|(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+))\s+(?:-|(({src_port}\d+?)|[^\s]+))\s+(?:-|(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+))\s+(?:-|(({dest_port}\d+?)|[^\s]+))\s+(?:-|({share_path}[^\s]+))\s+(?:-|({service_name}[^\s]+))\s+(?:-|({native_file_system}[^\s]+))\s+(?:-|({share_type}[^\s]+?))\s*""",
     """({protocol}smb)"""
  ]


}
```