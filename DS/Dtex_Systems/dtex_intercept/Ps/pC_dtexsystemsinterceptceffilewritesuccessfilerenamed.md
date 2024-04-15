#### Parser Content
```Java
{
Name = "dtexsystems-intercept-cef-file-write-success-filerenamed"
  Vendor = Dtex Systems
  Product = DTEX InTERCEPT
  TimeFormat = "epoch"
  Conditions = [ "CEF:", """|Dtex|""", """|FileRenamed|""" ]
  Fields = [
    """\Wstart=({time}\d{13})""",
    """\|Dtex\|([^\|]+\|){2}(FileSystemActivity\|)?({access}[^\|]+)\|""",
    """\WDevice_Name =(({domain}[^\\]+)\\+)?({host}[^\\\s]+)""",
    """\WUser_Name =(({domain}[^\\]+)\\+)?({user}[^\\\s]+)\s""",
    """\WProcess_Name =(?:\s+|({process_name}.+?)\s+)(\w+=|$)""",
    """\WProcess_Directory=(?:\s+|({process_dir}.+?)\s+)(\w+=|$)""",
    """\WDestination_File_Extension=({file_ext}[^\s]+)\s""",
    """\WDestination_File_Name =(?:\s+|({file_name}.+?)\s+)(\w+=|$)""",
    """\WDestination_File_Directory=(?:\s+|({file_dir}.+?)\s+)(\w+=|$)""",
    """\|Dtex\|([^\|]+\|){3}.*?➔\s+({file_path}.+?)\s\(.*?\)\|""",
    """Destination_File_Details=\{.*?"Type":\s+"({file_type}[^"]+)"\}""",
    """\WSource_File_Directory=(?:\s+|({src_file_dir}.+?)\s+)(\w+=|$)""",
    """\WSource_File_Name =(?:\s+|({src_file_name}.+?)\s+)(\w+=|$)""",
    """\WDestination_File_Size=({bytes}\d+)""",
    """"ImageDetails":\s+\{.*?"ProductName":\s+"({app}[^"]+)""""
  ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"


}
```