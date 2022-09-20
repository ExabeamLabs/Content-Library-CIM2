#### Parser Content
```Java
{
Name = microsoft-o365-sk4-process-create-success-processcreated
  Vendor = Microsoft
  Product = Office 365
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """ProcessCreationEvents"""", """"ProcessCommandLine":""", """"ActionType":"ProcessCreated"""" ]
  Fields = [
    """"time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """"AccountName":"({user}[^"]+)""",
    """"AccountDomain":"({domain}[^"]+)""",
    """"ProcessId":({process_id}\d+)""",
    """"FileName":"({process_name}[^"]+)""",
    """"ProcessCommandLine":"\s*({process_command_line}.+?)\s*",""",
    """"FolderPath":"({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^"\\\/]+))"""",
    """"MD5":"({hash_md5}[^"]+)""",
    """"ComputerName":"({host}[^"]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```