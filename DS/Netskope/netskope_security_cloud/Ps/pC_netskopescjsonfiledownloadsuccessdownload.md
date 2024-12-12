#### Parser Content
```Java
{
Name = netskope-sc-json-file-download-success-download
  Vendor = Netskope
  Product = Netskope Security Cloud
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  ExtractionType = json
  Conditions = [ """"type":""", """"activity":""", """"Download"""", """"object_type":""", """"File"""", """"act_user":""", """"src-application-name":""", """"Netskope"""" ]
  Fields = [
    """exa_json_path=$.time,exa_field_name=time"""
    """exa_json_path=$.event-name,exa_field_name=event_name"""
    """exa_json_path=$..activity,exa_field_name=operation"""
    """exa_json_path=$.src-ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$..user,exa_regex=(({email_address}[^@"\s]+@[^@"\s]+\.[^"\s]+)|(({domain}[^"@\\\/\s]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """exa_json_path=$..app,exa_field_name=app"""
    """exa_json_path=$..user-email,exa_regex=(({email_address}[^@"\s]+@[^@"\s]+\.[^"\s]+)|(({domain}[^"@\\\/\s]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """exa_json_path=$..user_name,exa_regex=(({full_name}[^\\\s"]+\s[^"\\]+)|(({domain}[^"\s\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
   ]
   DupFields = [ "object->file_name" ]
   ParserVersion = v1.0.0


}
```