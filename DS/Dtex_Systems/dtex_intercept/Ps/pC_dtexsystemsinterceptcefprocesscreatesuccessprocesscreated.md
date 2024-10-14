#### Parser Content
```Java
{
Name = dtexsystems-intercept-cef-process-create-success-processcreated
  Vendor = Dtex Systems
  Product = DTEX InTERCEPT
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Dtex|""", """|ProcessCreated|""" ]
  Fields = [
    """\Wstart=({time}\d{13})""",
    """\|Dtex\|([^\|]*\|){2}(ProcessActivity\|)?({operation_type}[^\|]+)\|""",
    """\|Dtex\|([^\|]*\|){3}Running\s*({process_path}({process_dir}(?:[^\s\|]+)?[\\\/]+)?({process_name}[^\\\/\|]+))\|""",
    """\|Dtex\|([^\|]*\|){3}Running\s*({path}.+?)\|""",
    """\WDevice_Name =(({domain}[^\\]+)\\+)?({host}[^\\\s]+)""",
    """"ProcessId":\s*"({process_id}\d+)"""",
    """\WProcess_Name =(?:\s*|({process_name}.+?)\s+)(\w+=|$)""",
    """\WUser_Name =(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s""",
    """\WProcess_Parameters="({path}({process_path}({process_dir}(?:[^"]+)?[\\\/]+)?({process_name}[^\\\/\)"]+)))""",
    """\Wreason=({process_command_line}.+?)\s+(\w+=|$)""",
  ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"


}
```