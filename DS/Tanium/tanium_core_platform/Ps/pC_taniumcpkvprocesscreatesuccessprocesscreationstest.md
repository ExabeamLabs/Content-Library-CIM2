#### Parser Content
```Java
{
Name = tanium-cp-kv-process-create-success-processcreationstest
  Vendor = Tanium
  Product = Tanium Core Platform
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSZ"
  Conditions = [ """ Tanium """, """Question="Exabeam-Process-Creations-Test"""", """ Start-Time="2""" ]
  Fields = [
    """({host}[\w.\-]+)\s+Tanium """,
    """\sEndpoint-Name ="(-|({dest_host}[\w.\-]+))"""",
    """\sStart-Time="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d)""",
    """\sUsername="(-|({user}[\w\.\-]{1,40}\$?))"""",
    """\sDomain="(-|({domain}[^"]+))"""",
    """\sMD5="(-|({hash_md5}[^"]+))"""",
    """\sCommand-Line="(-|({process_command_line}[^"]+))"""",
    """\sParent-Process-Path="(-|<Unknown Process>|({parent_process_path}({parent_process_dir}[^"]*?[\\\/]+)?({parent_process_name}[^"\\\/]+)))"""",
    """\sProcess-Path="(-|({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^"\\\/]+)))"""",
 ]
 ParserVersion = "v1.0.0"


}
```