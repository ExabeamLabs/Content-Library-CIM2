#### Parser Content
```Java
{
Name = microsoft-windows-kv-process-create-success-processid
  Vendor = Microsoft
  Product = Microsoft WMI Log
  TimeFormat = "yyyyMMddHHmmss.SSSSSS"
  Conditions = [ """ProcessName ="""", """ProcessId=""", """CommandLine="""" ]
  Fields = [
    """StartTime="({time}\d+\.\d+)""",
    """Host="({host}[^"]+)""",
    """ProcessId=({process_guid}.+?)\s+(\w+=|$)""",
    """CommandLine="*({process_command_line}[^"]+?)\s*"""",
    """Path="({path}[^"]+)""",
    """Path="({process_path}({process_dir}[^"]+?)({process_name}[^"\\]+))"""",
    """ProcessName ="({process_name}[^"]+)""",
  ]
  DupFields = [ "host->dest_host", "process_guid->process_id" ]
  ParserVersion = "v1.0.0"


}
```