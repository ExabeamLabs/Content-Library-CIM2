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
""""UserId\\*"+:[\s\\]*"+(({domain}[^"\\]+)\\+)?(({email_address}[^@"]+@[^."]+\.[^"]+?)|(SecurityComplianceAlerts|(Unknown|Sync|AirInvestigation|({user}[^"@\\\s]*))))"""",
"""\ssuser=[^"@=\s]*?@([\.\w+]+\.)?({email_domain}[^\.\s"]+?\.[^\s"\.\\]+)""",
""""UserId\\*"+:[\s\\]*"+({email_address}[^@"]+@[^."]+\.[^"]+?)"""",
""""UserId\\*"+:[\s\\"]*"+[^"]*?@([\.\w+]+\.)?({email_domain}[^\.\s"]+?\.[^\s"\.>]+)>?\s*"+""",
""""UserId":"\\*"(?![^@"]+?@[^\s"]+)({domain}[^"\\\/]+)[^"]*?(Unknown|Sync|AirInvestigation|({user}[^"\\\/@\s]+))\\"""",
""""(Workload|Application|Client)\\*"+:[\s\\]*"+({app}[^"\\]*)""",
"""\WdestinationServiceName\s*=({app}[^=]+?)\s+(\w+=|$)""",
"""Workload"*:"*({app}[^"]+)""",
"""Workload"*:\s*"*({app}[^"]+)"*\}""",
"""\WsourceServiceName =({app}[^=]+?)\s+(\w+=|$)""",
""""ObjectId\\*"+:"?[\s\\]*"+(|Unknown|Not Available|({object}[^"\\]+))"""",
""""SourceFileName":"({object}[^",]+)""",
"""\ssuser=(anonymous|SecurityComplianceAlerts|({email_address}[^\s]+@[^\s]+\.[^\s]+)|(Unknown|Sync|AirInvestigation|(({domain}[^\\"\s@]+)\\+)?({user}[^"\s@]+?)))\s""",
"""\ssuser=({email_address}[^=@"]+@[^.="]+\.[^=]+?)\s\w+=""",
"""\ssuser=[^=\s]*?@([\.\w+]+\.)?({email_domain}[^\.\s"]+?\.[^\s"\.>]+)""",
""""ItemName":"({email_subject}[^"]+)""",
"""Sender":"({sender}[^"]+)""",
""""Receivers":\[({email_recipients}"({dest_email_address}[^",]+)[^\]]+?)\],"""",
""""ClientIP"+:"+\[?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
"""UserAgent":\s*"({user_agent}[^"]+)"""",
"""DatasetName"*:\s*"*({data_set_name}[^"]+)""",
"""Workload"*:\s*"*({resource}[^"]+)"*""",
""""TargetUserOrGroupName":"({target}[^"]+)"""",
"""cs2=({group_name}[^=]+)\s+\w+=""",
""""IsSuccess":({result}[^\s,]+)""",
"""SourceRelativeUrl":"({dest_path}[^"]+?)\s*"""",
"""SiteUrl":"({site_url}[^"]+)"""",
""""MailboxPrimaryAddress":"({email_address}[^@"]+@[^."]+\.[^"]+?)""""
]


}
```