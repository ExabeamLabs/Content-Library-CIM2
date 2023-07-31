#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-file-workload
ParserVersion = v1.0.0
Vendor = Microsoft
Product = Microsoft 365
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [ """"Workload""", """"Operation""", """destinationServiceName =Office 365""" ]
Fields = [
""""CreationTime\\*"+:[\s\\]*"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
""""DeviceName":"(::ffff:)?({host}[\w\-.]+)"""",
""""Operation\\*"+:[\s\\]*"+({operation}[^"\\\.]*)""",
""""UserId\\*"+:[\s\\]*"+(({domain}[^"\\]+)\\+)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(SecurityComplianceAlerts|(Unknown|Sync|AirInvestigation|(\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|({user}[^"@\\\s]*))))"""",
"""\ssuser=[^"@=\s]*?@([\.\w+]+\.)?({email_domain}[^\.\s"]+?\.[^\s"\.\\]+)""",
""""UserId\\*"+:[\s\\]*"+({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""",
""""UserId\\*"+:[\s\\"]*"+[^"]*?@([\.\w+]+\.)?({email_domain}[^\.\s"]+?\.[^\s"\.>]+)>?\s*"+""",
""""UserId":"\\*"(?![^@"]+?@[^\s"]+)({domain}[^"\\\/]+)[^"]*?(Unknown|Sync|AirInvestigation|(\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|({user}[^"\\\/@\s]+))\\"""",
""""(Workload|Application|Client)\\*"+:[\s\\]*"+({app}[^"\\]*)""",
"""\WdestinationServiceName\s*=({app}[^=]+?)\s+(\w+=|$)""",
"""Workload"*:"*({app}[^"]+)""",
"""Workload"*:\s*"*({app}[^"]+)"*\}""",
"""\WsourceServiceName =({app}[^=]+?)\s+(\w+=|$)""",
""""Operation\\*":\\*"(File|Folder)[^\}]+?"ObjectId\\*"+:"?[\s\\]*"+(|Unknown|Not Available|({file_path}({file_dir}[^"]*?)({file_name}[^"\\\/]+?(\.({file_ext}[^"\\\/\.]+?))?)))\\*"""",
""""Operation\\*:\\*"(?!(File|Folder))[^\}]+?"ObjectId\\*"+:"?[\s\\]*"+(|Unknown|Not Available|({object}[^"]+?))\\*"""",
""""SourceFileName\\*":\\*"({file_name}[^"\\\/]+?(\.({file_ext}[^"\\\/\.]+?))?)\\*"""",
"""\ssuser=(anonymous|SecurityComplianceAlerts|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(Unknown|Sync|AirInvestigation|(\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|({user}[^"\s@]+?)))\s""",
"""\ssuser=({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)\s\w+=""",
"""\ssuser=[^=\s]*?@([\.\w+]+\.)?({email_domain}[^\.\s"]+?\.[^\s"\.>]+)""",
""""ItemName":"({email_subject}[^"]+)""",
"""Sender":"({src_email_address}[^"]+)""",
""""Receivers":\[({email_recipients}"({dest_email_address}[^",]+)[^\]]+?)\],"""",
""""ClientIP"+:"+\[?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
"""UserAgent":\s*"({user_agent}[^"]+)"""",
"""DatasetName"*:\s*"*({data_set_name}[^"]+)""",
"""Workload"*:\s*"*({resource}[^"]+)"*""",
""""TargetUserOrGroupName":"({target}[^"]+)"""",
"""cs2=({new_value}[^=]+)\s+\w+=""",
""""IsSuccess":({result}[^\s,]+)""",
"""SourceRelativeUrl":"({dest_path}[^"]+?)\s*"""",
"""SiteUrl":"({site_url}[^"]+)"""",
""""MailboxPrimaryAddress":"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""",
""""Key":"OsName".*?Value":"({os}[^"]+)""""
]


}
```