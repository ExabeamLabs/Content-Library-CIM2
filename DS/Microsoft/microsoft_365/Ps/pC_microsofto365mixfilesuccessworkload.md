#### Parser Content
```Java
{
Name = "microsoft-o365-mix-file-success-workload"
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """Workload""""
  """SharePoint"""
  """ItemType"""
]
Fields = [
  """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """"CreationTime\\*\"+:\\*\s*\"+({time}[^\\\"]+)"""
  """"CreationTime\\*\"+:\\*\s*\"+({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)"""
  """"host\\*\"+:\\*\s*\"+(::ffff:)?({host}[^\"\\]+)"""
  """"*SourceRelativeUrl\\*\"+:\\*\s*\"+({src_file_dir}[^\"]+)"""
  """\"*SourceFileName\\*\"+:\\*\s*\"+\s*({src_file_name}[^\"\\]+?(\.({src_file_ext}\w+))?)(,|\s*\")"""
  """\"*SourceFileExtension\\*"+:\\*\s*"+\s*({src_file_ext}[^"\\,\s']+)""",
  """"*ObjectId\\*":\s*\\*"([a-f0-9]{8}(?:-[a-f0-9]{4}){4}[a-f0-9]{8}|({src_file_path}({src_file_dir}[^"]*?)?({src_file_name}[^\/"]+?(\.({src_file_ext}[^\\\/.\s",']+))?)))"(?!u\d+)"""
  """Operation\\*"+:\\*\s*"+({operation}[^"\\,]+)""",
  """\"*ClientIP\\*\"+:\\*\s*\"+(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F:]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\%\d+)?(:({src_port}\d+))?"""
  """\"*UserAgent\\*\"+:\\*\s*\"+({user_agent}[^\"\\]+)\"*,"""
  """"UserSharedWith\\*\"+:\\*\s*\"+({dest_user}[^\"@\\]+)"""
  """\"*ItemType\\*\"+:\\*\s*\"+({file_type}[^\"\\]+)\"*,"""
  """"Workload\\*"+:\\*\s*"+({app}[^"\\,]+)"""
  """"NewValue\\*\"+:\\*\s*\"+({new_attribute}[^\"@\\]+)"""
  """\WfileType=({file_type}[^\s]+)"""
  """\Wsproc=({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
  """\WfilePermission=(|({file_permissions}.+?))(\s+\w+=|\s*$)"""
  """\Wduser=(|({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({dest_user}[^=]+?))(\s+\w+=|\s*$)"""
  """\Wsuser=(urn:spo:guest#)?(NOT-FOUND|Unknown|Sync|AirInvestigation|Sync Client|Office365 Backend Process|Device Registration Service|Microsoft Intune|Microsoft Teams Services|Microsoft Online Services|Office 365 SharePoint Online|anonymous|SecurityComplianceAlerts|SecurityComplianceInsights|(Microsoft\\[^@\s"]+)|EMPTY\.*|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|(({user_id}(\w+\-){4}\w+)|({user}[\w\.\-]{1,40}\$?)(@({domain}[^\s"]+)|\_({=domain}[^@=]+)#(ext|EXT)#@[^"=]+)?)))(\s+\w+=|\s*$)"""
  """"UserId\\*\"+:\\*\s*\"+((\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|(urn:spo:guest#)?(NOT-FOUND|Unknown|Sync|AirInvestigation|Sync Client|Office365 Backend Process|Device Registration Service|Microsoft Intune|Microsoft Teams Services|Microsoft Online Services|Office 365 SharePoint Online|anonymous|system|SecurityComplianceAlerts|SecurityComplianceInsights|AAD to SharePoint Sync|(Microsoft\\[^@\s"]+)|EMPTY\.*|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\\s@"]+)\\)?(app@sharepoint|system|({user}[\w\.\-]{1,40}\$?))(@({=domain}[^\s"]+)|\_({=domain}[^@"]+)#(ext|EXT)#@[^"]+)?|({full_name}[\w,\s]+?)))""""
  """src-account-name\":\"({account_name}[^\"]+)"""
  """"FileSizeBytes\\*"+:\s*({bytes}\d+)"""
  """"BrowserName":"({browser}[^"]+)"""",
  """"UserAgent":"({user_agent}[^"]+)""""
  """"FileSyncBytesCommitted":"({bytes}\d+)"""",
  """"AuthenticationType":"({auth_method}[^",]+)"""
  """"UserType":"*\s*({user_type}[^,}"]+)"*"""
  """"DestinationLabel":"({tag}[^"]+)""""
  """"CorrelationId":\s*"({correlation_id}[^"]+)""""
]
DupFields = [
  "operation->action"
  "src_file_path->file_url"
  "src_file_path"->"file_path"
  "src_file_dir"->"file_dir"
  "src_file_name"->"file_name"
  "src_file_ext"->"file_ext"
]
ParserVersion = "v1.0.0"


}
```