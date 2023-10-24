#### Parser Content
```Java
{
Name = "code42-incydr-json-file-success-oshostname"
  Vendor = "Code42"
  Product = "Code42 Incydr"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
    """"fileCategoryByExtension""""
    """"eventType""""
    """"osHostName"""
  ]
  Fields = [
    """"eventType"+:\s*"+({access}MODIFIED|DELETED|READ|CREATED)""",
    """"mimeTypeByExtension"+:\s*"+({mime}[^"]+)"""",
    """"tabUrl"+:\s*"+({url}[^"]+)"""",
    """"exposure"+:\s*\["*({log_source}[^"\]]+)"*\]""",
    """"processName":\s*"({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^"\\\/]+?))""""
    """"userUid"+:\s*"+({user_uid}[^"]+)"""",
    """"deviceUid"+:\s*"+({device_id}[^"]+)"""",
    """"publicIpAddress"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"domainName"+:\s*"+(({host}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({domain}[^"]+))"""",
    """"eventTimestamp"+:\s*"+({time}[^"]+)"""",
    """"filePath"+:\s*"+({file_path}[^"]+)"""",
    """"fileName"+:\s*"+({src_file_name}[^"]+)"""",
    """"fileCategory"+:\s*"+({file_type}[^"]+)"""",
    """"fileCategoryByExtension"+:\s*"+({file_ext}[^"]+)"""",
    """"fileSize"+:\s*({bytes}\d+)""",
    """"processOwner"+:\s*"+({user}[\w\.\-]{1,40}\$?)"""",
    """"md5Checksum"+:\s*"+({hash_md5}[^"]+)"""",
    """"sha256Checksum"+:\s*"+({hash_sha256}[^"]+)"""",
    """"deviceUserName"+:\s*"+({email_address}[^@"]+@[^\."]+\.[^"]+)"""",
    """"osHostName"+:\s*"+({dest_host}[^"]+)"""",
    """"windowTitle"+:\s*\["*({service_name}[^"\]]+)"*\]""",
    """"actor"+:"+(({email_address}[^"@]+@[^"@]+)|({user}[\w\.\-]{1,40}\$?))""",
  ]
  DupFields = [
    "file_path->file_dir"
    "dest_host->device_name"
    "src_file_name->file_name"
  ]
  ParserVersion = "v1.0.0"


}
```