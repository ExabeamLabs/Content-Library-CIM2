#### Parser Content
```Java
{
Name = "dg-ep-kv-file-write-success-operation11"
  Vendor = "Digital Guardian"
  Product = "Digital Guardian Endpoint Protection"
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Fields = [
	"""Agent_Local_Time="({time}\d+\/\d+\/\d\d\d\d\s\d+:\d+:\d+\s(AM|PM|am|pm))""",
	"""\w+\s\d\d\s\d\d:\d\d:\d\d\s*({host}[\w\-.]+)\s\w+=""",
	"""\sComputer_Name ="(({domain}[^\\]+)?\\?({src_host}[^"]+))""",
	"""\sUser_Name ="(({domain}[^\\]+)?\\?({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
	"""\sSource_Directory="({src_file_dir}[^=]+?)\s*"\s*\w+=""",
	"""\sDestination_Directory="({file_dir}[^=]+?)\s*"\s*\w+=""",
	"""\sDestination_File="({file_name}[^="]+?(\.({file_ext}[^"\s\.=]+))?)\s*"\s*\w+=""",
	"""\sOperation="({event_code}\d+)""",
	"""\sApplication="({process_name}[^"]+)""",
	"""\sSource_File="({src_file_name}[^="]+?(\.({src_file_ext}[^"\s\.=]+))?)\s*"\s*\w+=""",
  ]
  Conditions = [
    """ Agent_Local_Time=""""
    """ User_Name =""""
    """ Operation="11"""" 
  ]
  ParserVersion = "v1.0.0"


}
```