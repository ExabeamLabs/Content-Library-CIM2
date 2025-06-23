#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-file-workload
ExtractionType = json
ParserVersion = v1.0.0
Vendor = Microsoft
Product = Microsoft 365
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [ """"Workload""", """"Operation""", """destinationServiceName =Office 365""" ]
Fields = [
"""exa_json_path=$..Members[0:].DisplayName,exa_field_name=members""",
"""exa_json_path=$.Attendees[0:].DisplayName,exa_field_name=members""",
"""exa_json_path=$.Attendees[0:].InviterInfo.DisplayName,exa_field_name=additional_info""",
"""exa_json_path=$..CreationTime,exa_field_name=time"""
"""exa_json_path=$..DeviceName,exa_field_name=host"""
"""exa_json_path=$..Operation,exa_field_name=operation"""
"""exa_json_path=$..UserId,exa_field_name=user_upn"""
"""exa_json_path=$..Workload,exa_field_name=app"""
"""exa_regex="(Workload|Application|Client)\\*"+:[\s\\]*"+({app}[^"\\]*)"""
"""exa_regex="Operation\\*":\\*"(File|Folder)[^\}]+?"ObjectId\\*"+:"?[\s\\]*"+(|Unknown|Not Available|({file_path}({file_dir}[^"]*?)({file_name}[^"\\\/]+?(\.({file_ext}[^"\\\/\.]+?))?)))\\*"""",
"""exa_regex="Operation\\*:\\*"(?!(File|Folder))[^\}]+?"ObjectId\\*"+:"?[\s\\]*"+(|Unknown|Not Available|({object}[^"]+?))\\*"""",
"""exa_regex=\ssuser=(anonymous|SecurityComplianceAlerts|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|(Unknown|Sync|AirInvestigation|(\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s""",
"""exa_regex="Sender":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
"""exa_regex="Receivers":\[({email_recipients}"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\]]+?)\],"""",
"""exa_json_path=$..SourceFileName,exa_field_name=file_name"""
"""exa_json_path=$..ItemName,exa_field_name=email_subject"""
"""exa_json_path=$..SenderAddress,exa_regex=(<>|\\+|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"""
"""exa_json_path=$..ClientIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""exa_json_path=$..UserAgent,exa_field_name=user_agent"""
"""exa_json_path=$..MailboxPrimaryAddress,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""
"""exa_json_path=$..UserType,exa_field_name=user_type"""
"""exa_json_path=$..severity,exa_field_name=alert_severity"""
"""exa_json_path=$..correlationId,exa_field_name=correlation_id"""
"""exa_json_path=$..UserId,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
"""exa_json_path=$..SensitivityLabelId,exa_field_name=sensitivity_label"""
"""exa_json_path=$..OldSensitivityLabelId,exa_field_name=old_sensitivity_label"""
"""exa_json_path=$..LabelId,exa_field_name=label_id"""
"""exa_json_path=$..JustificationText,exa_field_name=additional_info"""
"""exa_json_path=$..ObjectId,exa_field_name=object_id"""
"""exa_json_path=$..documentEncrypted,exa_field_name=encrypted"""
"""exa_json_path=$..SourceRelativeUrl,exa_field_name=dest_process_path"""
"""exa_json_path=$..SiteUrl,exa_field_name=url"""
"""exa_json_path=$..IsSuccess,exa_field_name=result"""
"""exa_json_path=$..TargetUserOrGroupName,exa_field_name=target"""
"""exa_json_path=$..DatasetName,exa_field_name=file_name"""
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
""""ClientIP"+:"+\[?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
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
"""Severity\\?":\\?"({alert_severity}[^"\\]+)"""
""""Attendees":[^\]]+?"InviterInfo":[^\}]+?"DisplayName":"({additional_info}[^"]+)"""
""""Attendees":[^\]]+"DisplayName":"({member}[^"]+)"""
]
DupFields = [ "operation->alert_name"]


}
```