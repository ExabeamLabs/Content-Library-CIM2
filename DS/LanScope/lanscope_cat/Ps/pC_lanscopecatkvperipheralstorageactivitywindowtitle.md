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
    """\sLogonUser="({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """\sApplication="({process_name}[^"]+)""",
    """\sFileSize="({bytes}\d+)""",
    """\sDevice="({device_id}[^"]+)""",
    """\sIPAddress="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sWindowTitle="({file_path}(({file_dir}[^"]+?)[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))))"""",
  ]
  DupFields = [ "operation->access" ]
  ParserVersion = "v1.0.0"


}
```