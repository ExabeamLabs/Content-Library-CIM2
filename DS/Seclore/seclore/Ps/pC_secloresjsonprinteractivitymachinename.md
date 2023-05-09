#### Parser Content
```Java
{
Name = seclore-s-json-printer-activity-machinename
  Conditions = [ """"machine_name"""", """"activity":""", """"user_name":""", """"offline_access_right":""", """"activity":4""" ]
  Fields = ${SecloreDLParserTemplates.seclore-file-operations.Fields}[
    """"activity":({access}4)"""
  ]
  ParserVersion = "v1.0.0"

seclore-file-operations = {
  Vendor = Seclore
  Product = Seclore
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """"creation_time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""",
    """"machine_name":"({host}[^"]+)?"""",
    """"machine_ip1":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"user_name":"({full_name}[^"]+)"""",
    """"user_email_id":"({email_address}[^\@]+\@[^"]+)"""",
    """"current_file_name":"({file_name}[^"]+)"""",
    """"current_location":"({file_dir}[^"]+)?"""",
    """"source_location":"({src_file_dir}[^"]+)?"""",
    """"file_name":"({src_file_name}[^"]+)"""",
    """"activity_comments":"*(null|({additional_info}[^",]+))""",
    """"authorized":({result}\d+)"""
  
}
```