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
  """"CreationTime\\*\"+:\\*\s*\"+({time}[^\\\"]+)"""
  """"host\\*\"+:\\*\s*\"+(::ffff:)?({host}[^\"\\]+)"""
  """"SourceRelativeUrl\\*\"+:\\*\s*\"+({file_dir}[^\"]+)"""
  """"ObjectId\\*\"+:\\*\s*\"+({file_path}[^\"]+)[\\\"](?!\\u\d+)"""
  """\"*ObjectId\\*\"+:\\*\s*\"+({src_file_dir}[^\"]+)[\\\/](?!u\d+)"""
  """"ObjectId\\*\"+:\\*\s*\"+({file_url}[^\"]*?({src_file_name}[^\/\"]+?(\.({src_file_ext}[^\\\/\.\s\"]+))?))\"(?!u\d+)"""
  """Operation\\*"+:\\*\s*"+({operation}[^"\\,]+)""",
  """"UserId\\*\"+:\\*\s*\"+({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)\\*)""""
  """\"*ClientIP\\*\"+:\\*\s*\"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\"*UserAgent\\*\"+:\\*\s*\"+({user_agent}[^\"\\]+)\"*,"""
  """"UserSharedWith\\*\"+:\\*\s*\"+({object}[^\"@\\]+)"""
  """\"*SourceFileName\\*\"+:\\*\s*\"+\s*({file_name}[^\"\\]+?)\s*\""""
  """\"*SourceFileExtension\\*"+:\\*\s*"+\s*({file_ext}[^"\\,\s]+)""",
  """\"*ItemType\\*\"+:\\*\s*\"+({file_type}[^\"\\]+)\"*,"""
  """"Workload\\*"+:\\*\s*"+({app}[^"\\,]+)"""
  """"NewValue\\*\"+:\\*\s*\"+({object}[^\"@\\]+)"""
  """\WfilePath=\{.*?\"ObjectUrl\":\"({file_path}[^\"]+)\""""
  """\WfileType=({file_type}[^\s]+)"""
  """\Wsproc=({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
  """\WfilePermission=(|({permission_type}.+?))(\s+\w+=|\s*$)"""
  """\Wduser=(|({action_performer}[^=]+?))(\s+\w+=|\s*$)"""
  """\Wsuser=(|({affected_user}[^@\s]+@[^=]+?))(\s+\w+=|\s*$)"""
  """src-account-name\":\"({account_name}[^\"]+)"""
  """"FileSizeBytes\\*"+:\s*({bytes}\d+)"""
]
DupFields = [
  "operation->access"
  "file_name->object"
]
ParserVersion = "v1.0.0"


}
```