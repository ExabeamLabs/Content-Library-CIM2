#### Parser Content
```Java
{
Name = "code42-incydr-json-file-success-oshostname"
  Vendor = "Code42"
  Product = "Code42 Incydr"
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = [
    """"fileCategoryByExtension""""
    """"eventType""""
    """"osHostName"""
  ]
  Fields = [
    """"eventType"+:\s*"+({access}[^"]+)""",
    """"mimeTypeByExtension"+:\s*"+({mime}[^"]+)"""",
    """"tabUrl"+:\s*"+({url}[^"]+)"""",
    """"exposure"+:\s*\["*({log_source}[^"\]]+)"*\]""",
    """"processName":\s*"({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^"\\\/]+?))""""
    """"userUid"+:\s*"+({user_uid}[^"]+)"""",
    """"deviceUid"+:\s*"+({device_id}[^"]+)"""",
    """"publicIpAddress"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"domainName"+:\s*"(({host}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({domain}[^"]+))"""",
    """"eventTimestamp"+:\s*"+({time}[^"]+)"""",
    """"filePath"+:\s*"+({file_dir}[^"]+)"""",
    """"fileName"+:\s*"+({src_file_name}[^"]+?(\.({src_file_ext}[^"\s\.]+))?)"""",
    """"fileCategory"+:\s*"+({file_type}[^"]+)"""",
    """"fileCategoryByExtension"+:\s*"+({file_ext}[^"]+)"""",
    """"fileSize"+:\s*({bytes}\d+)""",
    """"processOwner"+:\s*"+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """"md5Checksum"+:\s*"+({hash_md5}[^"]+)"""",
    """"sha256Checksum"+:\s*"+({hash_sha256}[^"]+)"""",
    """"deviceUserName"+:\s*"+({email_address}[^@"]+@[^\."]+\.[^"]+)"""",
    """"osHostName"+:\s*"+({dest_host}[^"]+)"""",
    """"windowTitle"+:\s*\["*({requested_app}[^"\]]+)"*\]""",
    """"actor"+:"+(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-]{1,40}\$?))""",
    """exa_regex="eventType"+:\s*"+({access}MODIFIED|DELETED|READ|CREATED)""",
    """exa_json_path=$.mimeTypeByExtension,exa_field_name=mime""",
    """exa_json_path=$.tabUrl,exa_field_name=url""",
    """exa_json_path=$.exposure[0],exa_field_name=log_source""",
    """exa_regex="processName":\s*"({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^"\\\/]+?))"""",
    """exa_json_path=$.userUid,exa_field_name=user_uid""",
    """exa_json_path=$.deviceUid,exa_field_name=device_id""",
    """exa_json_path=$.publicIpAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.domainName,exa_regex=(({host}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({domain}[^"]+))""",
    """exa_json_path=$.eventTimestamp,exa_field_name=time""",
    """exa_json_path=$.filePath,exa_field_name=file_dir""",
    """exa_json_path=$.fileName,exa_regex=({src_file_name}[^"]+?(\.({src_file_ext}[^"\s\.]+))?)$""",
    """exa_json_path=$.fileCategory,exa_field_name=file_type""",
    """exa_json_path=$.fileCategoryByExtension,exa_field_name=file_ext""",
    """exa_json_path=$.fileSize,exa_field_name=bytes""",
    """exa_json_path=$.processOwner,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """exa_json_path=$.md5Checksum,exa_field_name=hash_md5""",
    """exa_json_path=$.sha256Checksum,exa_field_name=hash_sha256""",
    """exa_json_path=$.deviceUserName,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_json_path=$.osHostName,exa_field_name=dest_host""",
    """exa_json_path=$.windowTitle[0],exa_field_name=requested_app""",
    """exa_regex="actor"+:"+(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-]{1,40}\$?))"""
  ]
  DupFields = [
    "dest_host->device_name"
    "src_file_name->file_name"
    "src_file_ext->file_ext"
  ]
  ParserVersion = "v1.0.0"


}
```