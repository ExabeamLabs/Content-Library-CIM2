#### Parser Content
```Java
{
Name = cyberark-psm-kv-app-activity-success-otherinfo
    Vendor = CyberArk
    Product = Privileged Session Manager
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """Operation:""", """ObjectType:""", """OtherInfo:""" ]
    Fields = [
                """Operation: ({operation}.*?) ObjectType""",
                """:\d\d\s({host}[^=]+)\sPAR""",
                """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
                """(AdminName|UserName): ({user}[^\s].+)\sOperation""",
                """Failed\?\s({event_subtype}\d)\s""",
                """Target: ({app}[^\s].+)\sRole""",
                """OtherInfo:\s({additional_info}.+)\s""",
                """Role:\s({app_group}.+?)\s"""
    ]
	ParserVersion = "v1.0.0"


}
```