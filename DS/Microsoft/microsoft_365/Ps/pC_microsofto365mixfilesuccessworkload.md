#### Parser Content
```Java
{
Name = "microsoft-o365-mix-file-success-workload"
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """Workload"""
  """SharePoint"""
  """ItemType"""
]
Fields = [
  """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """"CreationTime\\*\"+:\\*\s*\"+({time}[^\\\"]+)"""
  """"CreationTime\\*\"+:\\*\s*\"+({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)"""
  """"host\\*\"+:\\*\s*\"+(::ffff:)?({host}[^\"\\]+)"""
  """"*SourceRelativeUrl\\*\"+:\\*\s*\"+({src_file_dir}[^\"]+)"""
  """"*ObjectId\\*":\s*\\*"({file_path}({file_dir}[^"]*?)?({file_name}[^\/"]+?(\.({file_ext}[^\\\/.\s",]+))?))(,|\")(?!u\d+)"""
  """Operation\\*"+:\\*\s*"+({operation}[^"\\,]+)""",
  """"UserId\\*\"+:\\*\s*\"+(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)\\*)|({user}[\w\.\-]{1,40}\$?))""""
  """\"*ClientIP\\*\"+:\\*\s*\"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F:]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\"*UserAgent\\*\"+:\\*\s*\"+({user_agent}[^\"\\]+)\"*,"""
  """"UserSharedWith\\*\"+:\\*\s*\"+({dest_user}[^\"@\\]+)"""
  """\"*SourceFileName\\*\"+:\\*\s*\"+\s*({src_file_name}[^\"\\]+?)(,|\s*\")"""
  """\"*SourceFileExtension\\*"+:\\*\s*"+\s*({src_file_ext}[^"\\,\s]+)""",
  """\"*ItemType\\*\"+:\\*\s*\"+({file_type}[^\"\\]+)\"*,"""
  """"Workload\\*"+:\\*\s*"+({app}[^"\\,]+)"""
  """"NewValue\\*\"+:\\*\s*\"+({new_attribute}[^\"@\\]+)"""
  """\WfilePath=\{.*?\"ObjectUrl\":\"({file_path}[^\"]+)\""""
  """\WfileType=({file_type}[^\s]+)"""
  """\Wsproc=({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
  """\WfilePermission=(|({permission_type}.+?))(\s+\w+=|\s*$)"""
  """\Wduser=(|({action_performer}[^=]+?))(\s+\w+=|\s*$)"""
  """\Wsuser=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|(({user_id}(\w+\-){4}\w+)|({user}[\w\.\-]{1,40}\$?)(@({domain}[^\s"]+))?))"""
  """\Wsuser=(|({affected_user}[^@\s]+@[^=]+?))(\s+\w+=|\s*$)"""
  """src-account-name\":\"({account_name}[^\"]+)"""
  """"FileSizeBytes\\*"+:\s*({bytes}\d+)"""
  """"BrowserName":"({browser}[^"]+)"""",
  """"UserAgent":"({user_agent}[^"]+)""""
  """"FileSyncBytesCommitted":"({bytes}\d+)"""",
  """"AuthenticationType":"({auth_method}[^",]+)"""
]
DupFields = [
  "operation->action"
  "file_path->file_url"
  "src_file_dir->src_file_path"
]
ParserVersion = "v1.0.0"


}
```