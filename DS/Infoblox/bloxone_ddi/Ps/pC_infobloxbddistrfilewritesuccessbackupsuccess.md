#### Parser Content
```Java
{
Name = infoblox-bddi-str-file-write-success-backupsuccess
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """manage_scheduled_backups[""", """: Backup to LOCAL was successful""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s+({host}[\w.-]+)\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)(:({src_port}\d+))?\s+({additional_info}[^~]+?)\s*$""",
    """Backup file ({file_path}({file_dir}[^"]+\/)?({file_name}([^\/.]+)(\.({file_ext}[^\."\s]+))?([\.\w]*)))""",
    """({event_name}Backup to LOCAL was successful)"""
   ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"


}
```