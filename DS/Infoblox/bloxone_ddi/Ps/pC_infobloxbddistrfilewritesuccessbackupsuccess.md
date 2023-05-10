#### Parser Content
```Java
{
Name = infoblox-bddi-str-file-write-success-backupsuccess
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """manage_scheduled_backups[""", """: Backup to LOCAL was successful""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s+({host}[\w.-]+)\s+({src_ip}[a-fA-F\d.:]+?)\s+({additional_info}[^~]+?)\s*$""",
    """Backup file ({file_path}({file_dir}[^"]+\/)?({file_name}([^\/.]+)(\.({file_ext}[^"\s]+))?))"""
   ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"


}
```