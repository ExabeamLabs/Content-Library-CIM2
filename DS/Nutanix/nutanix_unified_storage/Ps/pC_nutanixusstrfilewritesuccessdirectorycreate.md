#### Parser Content
```Java
{
Name = nutanix-us-str-file-write-success-directorycreate
  ParserVersion = "v1.0.0"
  Conditions = ["""|DirectoryCreate|success|""", """ SMB["""]
  Fields = ${NutanixFilesParserTemplates.nutanixfiles-events.Fields} [
    """({user_sid}[^|]+)\|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\|({event_name}DirectoryCreate)\|({result}success)"""
  ]

nutanixfiles-events = {
    Vendor = Nutanix
    Product = Nutanix Unified Storage
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
      """SMB\[[^]]+\]:[^\\]+\\({domain}[^\\]+)\\({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
      """SMB\[[^\|]+\|([^\|]*\|){4}({file_path}({file_dir}[^|]+)\/({file_name}[^\|\/]+?(\.({file_ext}[^\|\.]+))?))\|""",
      """\d\d:\d\d:\d\d\s+({host}[\w\-.]+)\s+SMB\[""",
    
}
```