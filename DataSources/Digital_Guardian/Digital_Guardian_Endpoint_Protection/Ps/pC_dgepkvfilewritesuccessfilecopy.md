#### Parser Content
```Java
{
Name = dg-ep-kv-file-write-success-filecopy
  Vendor = Digital Guardian
  Product = Digital Guardian Endpoint Protection
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = ["""Agent_UTC_Time=""","""Was_Destination_Removable="True"""", """Destination_Drive_Type="Removable"""", """Operation="File Copy"""" ]
  Fields = [
    """Agent_UTC_Time="({time}\d+\/\d+\/\d\d\d\d \d+:\d+:\d+ (am|AM|pm|PM))""",
    """Computer_Name ="([^\\]+\\)?({src_host}[^"]+)"""",
    """User_Name ="(({domain}[^\\]+)\\)?({user}[^"]+)"""",
    """Source_Directory="({src_file_dir}[^"]+)"""",
    """Source_File="({src_file_name}[^"]+)"""",
    """Destination_Directory="({file_dir}[^"]+)"""",
    """Destination_File="({src_file_name}[^"]+)"""",
    """Destination_File_Extension="({src_file_ext}[^"]+)"""",
    """Application="({process_name}[^"]+)"""",
    """Operation="({event_code}[^"]+)"""",
    """Bytes_Written="({bytes}\d+)"""",
    """Given_Name ="({first_name}[^"]+)"""",
    """Surname="({last_name}[^"]+)"""",
    """Email_Address="({email_address}[^@]+@[^.]+\.[^"]+)""""
  ]
  ParserVersion = v1.0.0


}
```