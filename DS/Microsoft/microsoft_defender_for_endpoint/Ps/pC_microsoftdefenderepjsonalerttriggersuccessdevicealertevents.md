#### Parser Content
```Java
{
Name = "microsoft-defenderep-json-alert-trigger-success-devicealertevents"
ParserVersion = v1.0.0
Conditions = [""""Category":""", """subject=AdvancedHunting-DeviceAlertEvents""", """"operationName""""]
Fields = ${MicrosoftParserTemplates.cef-defender-atp-2.Fields} [
"""Category":\s*"({alert_name}[^"]+)""",
"""Title":\s*"({additional_info}[^"]+)""",
"""FileName":\s*"({process_name}[^"]+)""",
"""Severity":\s*"({alert_severity}[^"]+)""",
"""AlertId":\s*"({alert_id}[^"]+)"""
"""DeviceName":\s*"({src_host}[^"]+)""",
]
DupFields = [ "category->alert_type" ]

cef-defender-atp-2 = {
     Vendor = Microsoft
     Product = Microsoft Defender for Endpoint
     TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
     Fields = [
       """time"+:\s*"+({time}[^"]+)"""",
       """operationName"+:\s*"+({operation}[^"]+)""",
       """category"+:\s*"+({category}[^"]+)""",
       """RemotePort"+:({dest_port}\d+)""",
       """RemoteIP"+:\s*"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
       """"Protocol"+:\s*"+({protocol}[^"]+)""",
       """LocalIP"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
       """LocalPort"+:({src_port}\d+)""",
       """ActionType"+:\s*"+({result}[^"]+)""",
       """DeviceName"+:\s*"+({dest_host}[\w\-.]+)""",
       """InitiatingProcessAccountName"+:\s*"+((?i)SYSTEM|(?i)network service|({user}[\w\.\-]{1,40}\$?))""",
       """"ProcessIntegrityLevel"+:\s*"+({process_integrity}[^"]+)""",
       """InitiatingProcessAccountSid"+:\s*"+({user_sid}[^"]+)""",
       """"InitiatingProcessFolderPath":\s*"({process_path}(({process_dir}[^"]+?)\\+)?({process_name}[^"\\]+))""""
       """InitiatingProcessFileName"+:\s*"+({process_name}[^"]+)""",
     ]
     DupFields = ["category->event_name"
}
```