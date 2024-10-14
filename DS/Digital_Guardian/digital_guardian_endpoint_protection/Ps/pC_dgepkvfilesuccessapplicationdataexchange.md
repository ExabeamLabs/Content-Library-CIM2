#### Parser Content
```Java
{
Name = "dg-ep-kv-file-success-applicationdataexchange"
Vendor = "Digital Guardian"
Product = "Digital Guardian Endpoint Protection"
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
"""Agent_UTC_Time="""
"""Was_Destination_Removable="False""""
"""Destination_Drive_Type="None""""
"""Operation="Application Data Exchange""""
]
Fields = [
"""Agent_UTC_Time="({time}\d+\/\d+\/\d\d\d\d \d+:\d+:\d+ (am|AM|pm|PM))"""
"""Computer_Name ="([^\\]+\\)?({src_host}[^"]+)""""
"""User_Name ="(({domain}[^\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
"""Source_Directory="(\?:\\|({src_file_dir}[^"]+))""""
"""Source_File="({src_file_name}[^"]+?(\.({src_file_ext}[^"\s\.=]+))?)\s*""""
"""Destination_Directory="(\?:\\|({file_dir}[^"]+))""""
"""Destination_File="({file_name}[^"]+?)\s*""""
"""Destination_File_Extension="({file_ext}[^"]+)"\s"""
"""Application="({process_name}[^"]+)""""
"""Operation="({event_code}[^"]+)""""
"""Bytes_Written="({bytes}\d+)""""
"""Given_Name ="({first_name}[^"]+)""""
"""Surname="({last_name}[^"]+)""""
"""Email_Address="({email_address}[^@]+@[^.]+\.[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```