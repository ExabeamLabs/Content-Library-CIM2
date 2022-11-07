#### Parser Content
```Java
{
Name = dg-ep-kv-process-create-success-applicationfullname
  Vendor = Digital Guardian
  Product = Digital Guardian Endpoint Protection
  TimeFormat = "M/d/yyyy H:mm:ss a"
  Conditions = [ """ Application_Full_Name ="""", """ Command_Line="""", """ Process_Created_Local_Time="""" ]
  Fields = [
    """\sAgent_Begin_UTC_Time="({time}\d+/\d+/\d\d\d\d \d+:\d+:\d+ (am|AM|pm|PM))""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w.\-]+)""",
    """Computer_Name ="([^\\]*\\)?({host}[^"]+?)"""",
    """\sApplication="\s*({process_name}[^"]+?)\s*"""",
    """\sApplication_Directory="({process_dir}[^"]+)""",
    """\sParent_Application="\s*({parent_process_name}[^"]+?)\s*"""",
    """\sComputer_Type="({os}[^"]+)""",
    """\sMD5_Checksum="({hash_md5}[^"]+)""",
    """\sUser_Name ="(({domain}[^"\\]+)\\+)?({user}[^\\"]+)""",
    """\sProcess_File_Size="({bytes}\d+)""",
    """\sCommand_Line="\s*({process_command_line}.+?)\s*" \#\d+""",
  ]
  ParserVersion = v1.0.0


}
```