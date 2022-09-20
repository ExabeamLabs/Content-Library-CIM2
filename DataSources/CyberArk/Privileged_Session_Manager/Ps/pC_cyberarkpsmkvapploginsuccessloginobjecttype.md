#### Parser Content
```Java
{
Name = cyberark-psm-kv-app-login-success-loginobjecttype
    Vendor = CyberArk
    Product = Privileged Session Manager
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """Operation: Login ObjectType:""" ]
    Fields = [
                """:\d\d\s({host}[^=]+)\sPAR""",
                """({src_ip}\d+\.\d+\.\d+\.\d+)""",
                """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
                """(AdminName|UserName): ({user}[^\s]*)\s""",
                """TargetURL=({app}.+?).\s""",
                """OtherInfo: ({protocol}.*?)\s+TargetURL""",
                """PAR\[({event_code}\d+)""",
                """ObjectType:\s({event_subtype}.+)\sTarget:"""
    ]
	ParserVersion = "v1.0.0"


}
```