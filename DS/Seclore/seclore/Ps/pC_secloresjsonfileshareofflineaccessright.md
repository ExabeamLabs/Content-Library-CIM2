#### Parser Content
```Java
{
Name = seclore-s-json-file-share-offlineaccessright
  Conditions = [ """"machine_name"""", """"activity":""", """"user_name":""", """"offline_access_right":""", """"activity":5""" ]
  ExtractionType = json
  ParserVersion = "v1.0.0"

seclore-file-operations = {
  Vendor = Seclore
  Product = Seclore
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """exa_json_path=$.creation_time,exa_field_name=time""",
    """exa_json_path=$.machine_name,exa_regex=(|({host}.+))$""",
    """exa_json_path=$.machine_ip1,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """exa_json_path=$.user_name,exa_field_name=full_name""",
    """exa_json_path=$.user_email_id,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_json_path=$.current_file_name,exa_field_name=file_name""",
    """exa_json_path=$.current_location,exa_field_name=file_dir""",
    """exa_json_path=$.source_location,exa_field_name=src_file_dir""",
    """exa_json_path=$.file_name,exa_field_name=src_file_name""",
    """exa_json_path=$.activity_comments,exa_regex=(null|({additional_info}[^",]+))""",
    """exa_json_path=$.authorized,exa_field_name=result""",
    """exa_json_path=$.activity,exa_field_name=access"""
  
}
```