#### Parser Content
```Java
{
Name = mcafee-es-kv-file-write-success-removalstorage
    Vendor = McAfee
    Product = McAfee Endpoint Security
    TimeFormat = "epoch"
    Conditions = [ """|McAfee|ESM|""", """|359-""", """OUTGOING_FS_REMOVABLE_STORAGE""", """EVDNC|MON|OFF""" ]
    Fields = [
      """\send=({time}\d{13})""",
      """\sdeviceTranslatedAddress=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """\sshost=({src_host}[^\s]+)""",
      """\snitroObject_Type=({operation}.+?)\s[^\s]+?=""",
      """\snitroThreat_Name =({operation_details}.+?)\s[^\s]+?=""",
      """\sduser=([^\\=]+?\\)?({user}.+?)\s[^\s]+?=""",
      """\sdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """\snitroProcess_Name =({process_path}({process_dir}(?:[^=]+)?[\\\/])?({process_name}[^\\\/=]+))\s[^\s]+="""
    ]
	ParserVersion = "v1.0.0"
  

}
```