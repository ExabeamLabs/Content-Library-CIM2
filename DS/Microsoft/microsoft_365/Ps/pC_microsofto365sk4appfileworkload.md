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
""""UserId\\*"+:[\s\\]*"+({user_upn}[^",]+)"""",
""""(Workload|Application|Client)\\*"+:[\s\\]*"+({app}[^"\\]*)""",
"""destinationServiceName\s*=({app}[^=]+?)\s+(\w+=|$)""",
"""Workload"*:"*({app}[^"]+)""",
"""Workload"*:\s*"*({app}[^"]+)"*\}""",
"""\WsourceServiceName =({app}[^=]+?)\s+(\w+=|$)""",
""""Operation\\*":\\*"(File|Folder)[^\}]+?"ObjectId\\*"+:"?[\s\\]*"+(|Unknown|Not Available|({file_path}({file_dir}[^"]*?)({file_name}[^"\\\/]+?(\.({file_ext}[^"\\\/\.]+?))?)))\\*"""",
""""Operation\\*:\\*"(?!(File|Folder))[^\}]+?"ObjectId\\*"+:"?[\s\\]*"+(|Unknown|Not Available|({object}[^"]+?))\\*"""",
""""SourceFileName\\*":\\*"({file_name}[^"\\\/]+?(\.({file_ext}[^"\\\/\.]+?))?)\\*"""",
"""\ssuser=(anonymous|SecurityComplianceAlerts|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|(Unknown|Sync|AirInvestigation|(\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s""",
""""ItemName":"({email_subject}[^"]+)""",
""""Sender":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
""""Receivers":\[({email_recipients}"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\]]+?)\],"""",
""""ClientIP"+:"+\[?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
"""UserAgent":\s*"({user_agent}[^"]+)"""",
"""DatasetName"*:\s*"*({file_name}[^"]+)""",
"""Workload"*:\s*"*({resource}[^"]+)"*""",
""""TargetUserOrGroupName":"({target}[^"]+)"""",
"""cs2=({new_value}[^=]+)\s+\w+=""",
""""IsSuccess":({result}[^\s,]+)""",
"""SourceRelativeUrl":"({dest_process_path}[^"]+?)\s*"""",
"""SiteUrl":"({url}[^"]+)"""",
""""MailboxPrimaryAddress":"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""",
"""("Value":"({os}[^"]+)",)?"Key":"OsName"(,"Value":"({=os}[^"]+)")?"""
""""UserType":({user_type}[^,\}"]+)"*"""
""""correlationId":\s*"({correlation_id}[^"]+)""""
""""SensitivityLabelId":"({sensitivity_label}[^",]+)""""
""""OldSensitivityLabelId":"({old_sensitivity_label}[^",]+)""""
""""documentEncrypted":({encrypted}[^",]+)"""
""""ObjectId":"({object_id}[^",]+)""""
""""JustificationText":"({additional_info}[^",]+)""""
""""LabelId":"({label_id}[^",]+)"""
""""UserId":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
]


}
```