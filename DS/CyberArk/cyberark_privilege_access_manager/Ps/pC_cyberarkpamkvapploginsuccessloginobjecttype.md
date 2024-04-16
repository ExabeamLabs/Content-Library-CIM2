#### Parser Content
```Java
{
Name = cyberark-pam-kv-app-login-success-loginobjecttype
    Vendor = CyberArk
    Product = "CyberArk Privilege Access Manager"
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """Operation: Login ObjectType:""" ]
    Fields = [
                """:\d\d\s({host}[^=]+)\sPAR""",
                """({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
                """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
                """(AdminName|UserName): ({user}[\w\.\-]{1,40}\$?)\s""",
                """TargetURL=({app}.+?).\s""",
                """OtherInfo: ({protocol}.*?)\s+TargetURL""",
                """PAR\[({event_code}\d+)""",
                """ObjectType:\s({event_subtype}.+)\sTarget:"""
    ]
	ParserVersion = "v1.0.0"


}
```