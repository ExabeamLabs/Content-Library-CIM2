#### Parser Content
```Java
{
Name = mcafee-es-kv-file-write-success-removalstorage
    Vendor = McAfee
    Product = McAfee Endpoint Security
    TimeFormat = "epoch"
    Conditions = [ """|McAfee|ESM|""", """|359-""", """OUTGOING_FS_REMOVABLE_STORAGE""", """EVDNC|MON|OFF""" ]
    Fields = [
      """\send=({time}\d+)""",
      """\sdeviceTranslatedAddress=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """\ssrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """\sshost=({src_host}[^\s]+)""",
      """\snitroObject_Type=({operation}.+?)\s[^\s]+?=""",
      """\snitroThreat_Name =({activity_details}.+?)\s[^\s]+?=""",
      """\sduser=([^\\=]+?\\)?({user}.+?)\s[^\s]+?=""",
      """\sdst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """\snitroProcess_Name =({process_path}({process_dir}(?:[^=]+)?[\\\/])?({process_name}[^\\\/=]+))\s[^\s]+="""
    ]
	ParserVersion = "v1.0.0"
  

}
```