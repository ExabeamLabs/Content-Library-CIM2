#### Parser Content
```Java
{
Name = lanscope-cat-kv-peripheral-storage-activity-windowtitle
  Vendor = LanScope
  Product = LanScope Cat
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """LanScopeCat - Operation""", """WindowTitle=""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d)\s+({host}\S+)\s+LanScopeCat\s+\-""",
    """\sEvent="({operation}[^"]+)""",
    """\sAgent="({dest_host}[^"]+)""",
    """\sLogonUser="({user}[^"]+)""",
    """\sApplication="({process_name}[^"]+)""",
    """\sFileSize="({bytes}\d+)""",
    """\sDevice="({device_id}[^"]+)""",
    """\sIPAddress="({src_ip}[a-fA-F\d.:]+)""",
    """\sWindowTitle="({file_path}(({file_dir}[^"]+?)[\\\/]+)?({file_name}[^"\\\/]+))"""",
  ]
  ParserVersion = "v1.0.0"


}
```