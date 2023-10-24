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
    ""","ipAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    ""","profileId":"({user_id}\d+)""",
    """"actor":\{[^=]*?"email":"(({email_address}[^@"]+@[^@"]+)|({user}[\w\.\-]{1,40}\$?))"""",
    ""","events":[^=]*?"name"\s*:\s*"old_value",\s*"multiValue"\s*:\s*\[\s*"({src_file_name}[^"]+)"""",
    ""","events":[^=]*?"name"\s*:\s*"new_value",\s*"multiValue"\s*:\s*\[\s*"\s*({file_name}[^"]+?)\s*"""",
    ""","events":[^=]*?"name":"({access}[^"]+)"""",
    ""","events":[^=]*?"type":"access","name":"({access}[^"]+)"""",
    ""","events":[^=]*?"name"\s*:\s*"destination_folder_title",\s*"value"\s*:\s*"({file_dir}[^"]+)"""",
    ""","events":[^=]*?"name"\s*:\s*"source_folder_title",\s*"value"\s*:\s*"({src_file_dir}[^"]+)"""",
    """:"doc_id","value":"({file_id}[^"]+)"""",
    """:"doc_type","value":"(unknown|({file_type}[^"]+))"""",
    """:"doc_title","value":"\s*({file_name}[^"]+?)\s*"""",
    """:"visibility","value":"({privileges}[^"]+)"""",
    """:"owner","value":"\s*({file_owner}[^"]+?)\s*"""",
    """\sdestinationServiceName =({service_name}[^=]+?)\s+\w+=""",
    """"applicationName":"({app}[^"]+)"""",
    """"kind":\s*"({category}[^"]+)"""
    """suser=(?=[^\s]+@[^\s]+)({user}[\w\.\-]{1,40}\$?)@({domain}[^\s@]+)\s+(\w+=|$)"""
    """:"owner","value":"\s*({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)\s*""""
  ]
  DupFields = [ "access->operation", "email_address->src_email_address" ]
  ParserVersion = "v1.0.0"


}
```