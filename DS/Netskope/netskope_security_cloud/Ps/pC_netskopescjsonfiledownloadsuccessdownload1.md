#### Parser Content
```Java
{
Name = "netskope-sc-json-file-download-success-download-1"
  Vendor = "Netskope"
  Product = "Netskope Security Cloud"
  ExtractionType = json
  TimeFormat = "epoch_sec"
  Conditions = [  """"type":"""", """"ccl":""", """"activity":"Download"""", """"object_type":"File"""" ]
  Fields = [
    """exa_json_path=$.hostname,exa_field_name=src_host"""
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.app,exa_field_name=app"""
    """exa_json_path=$.srcip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.object,exa_regex=({file_name}[^"]+?(\.({file_ext}[^"\.\s\\\/]+?))?)"""
    """exa_json_path=$.object_type,exa_field_name=object_type"""
    """exa_json_path=$.user,exa_regex=(unknown|(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|(({domain}[^\s"@\\\/]+)[\\\/]+)?(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({user}[\w\.\-\!\#\^\~]{1,40}\$?))))"""
    """exa_json_path=$.access_method,exa_field_name=auth_method"""
    """exa_json_path=$.logintype,exa_field_name=auth_method"""
    """exa_json_path=$.activity,exa_field_name=operation"""
    """exa_json_path=$.url,exa_field_name=url"""
    """exa_json_path=$.file_size,exa_field_name=bytes"""
    """exa_json_path=$.file_type,exa_field_name=file_type"""
    """exa_json_path=$.page_site,exa_field_name=app"""
    """exa_json_path=$.dstport,exa_field_name=dest_port"""
    """exa_json_path=$.action,exa_field_name=action"""
    """exa_json_path=$.referer,exa_field_name=referrer"""
    """exa_json_path=$.useragent,exa_field_name=user_agent"""
    """exa_json_path=$.src_location,exa_field_name=src_location"""
    """exa_json_path=$.src_country,exa_field_name=src_country"""
    """exa_json_path=$.dstip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """exa_json_path=$.useragent,exa_field_name=user_agent"""
    """exa_regex="object":\s*"(Unknown Unknown|unknown|Unknown|null|\s*(|({object}[^"]+?)))\s*"[^\}]*?"object_type":\s*"(?!(File|Image|Folder|User))({object_type}[^"]+)""""
    """exa_regex="object":\s*"({file_name}[^"\\\/]+?(\.({file_ext}[^"\.\s\\\/]+?))?)"[^\}]*?"activity":\s*"File\w+""""
    """exa_regex="object_type":\s*"(File|Image)"[^\}]*?"object":\s*"\s*({file_name}[^"]+?(\.({file_ext}[^"\.\s\\\/]+?))?)""""
    """exa_regex="object_type":\s*"Folder"[^\}]*?"object":\s*"\s*(({folder_name}[^"\\\/]+)|({file_dir}[^"\/\\]+[\/\\]+[^"]+))""""
    """exa_regex="activity":\s*"File\w+"[^\}]*?"object":\s*"({file_name}[^"\\\/]+?(\.({file_ext}[^"\.\s\\\/]+?))?)""""
    """exa_json_path=$.url,exa_regex=({file_url}({file_path}({file_dir}[^"]+\/)({file_name}[^"]+?(\.({file_ext}[^"\\\/\.]+))?)?))"""
    """exa_regex="object":\s*"'?\s*({file_dir}[^"]+\/)?({file_name}[^"]+(\.({file_ext}\w+)?))".*"object_type":"(File|Image)""""
    """exa_regex=""object_type":"File",.*"object":\s*"'?\s*({file_dir}[^"]+\/)?({file_name}[^"]+(\.({file_ext}\w+)?))""""
  ]
  DupFields = [ "file_type->mime" ]
  ParserVersion = "v1.0.0"


}
```