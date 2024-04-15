#### Parser Content
```Java
{
Name = "google-workspace-cef-file-success-drive"
Vendor = "Google"
Product = "Google Workspace"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [ """"applicationName":""", """"drive"""", """"uniqueQualifier":""",  """"access"""" ]
Fields = [
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s(::ffff:)?({host}[\w\-.]+)\s\d+\s""",
    ""","time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""",
    ""","ipAddress":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    ""","profileId":"({user_id}\d+)""",
    """"actor":\{[^=]*?"email":"(({email_address}[^@"]+@[^@"]+)|({user}[^@"\s]+))"""",
    ""","events":[^=]*?"name"\s*:\s*"old_value",\s*"multiValue"\s*:\s*\[\s*"({src_file_name}[^"]+)"""",
    ""","events":[^=]*?"name"\s*:\s*"new_value",\s*"multiValue"\s*:\s*\[\s*"\s*({file_name}[^"]+?)\s*"""",
    ""","events":[^=]*?"name":"({access}[^"]+)"""",
    ""","events":[^=]*?"type":"access","name":"({access}[^"]+)"""",
    ""","events":[^=]*?"name"\s*:\s*"destination_folder_title",\s*"value"\s*:\s*"({file_dir}[^"]+)"""",
    ""","events":[^=]*?"name"\s*:\s*"source_folder_title",\s*"value"\s*:\s*"({src_file_dir}[^"]+)"""",
    ""","events":[^=]*?"name":"doc_id","value":"({file_id}[^"]+)"[^=]*?"name":"doc_type","value":"(unknown|({file_type}[^"]+))"[^=]*?"name":"doc_title","value":"\s*({file_name}[^"]+?)\s*"[^=]*?"name":"visibility","value":"({privileges}[^"]+)"[^=]*?"name":"owner","value":"\s*({file_owner}[^"]+?)\s*"\},((\{[^}]+\},\{[^\}]*?"value":"({additional_info}[^"]+))?)"""
  ]
  DupFields = [ "file_name->object", "privileges->operation" ]

ParserVersion = "v1.0.0"


}
```