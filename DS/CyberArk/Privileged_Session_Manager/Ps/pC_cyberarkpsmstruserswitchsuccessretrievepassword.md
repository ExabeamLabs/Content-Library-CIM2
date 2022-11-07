#### Parser Content
```Java
{
Name = cyberark-psm-str-user-switch-success-retrievepassword
    Vendor = CyberArk
    Product = Privileged Session Manager
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """Operation: Retrieve Password ObjectType:""" ]
    Fields = [
        """Operation: ({operation}.*?) ObjectType""",
	"""({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
	"""(AdminName|UserName):\s({user}.+)\sOperation""",
	"""Target:\s*(?:({dest_domain}[^\\\/]+)[\\\/]+)?({dest_user}.+?)\s*Role:""",
	""":\d\d\s({host}[^=]+)\sPAR""",
	"""PAR\[({event_code}\d+)"""
    ]
    DupFields = [ "host->dest_host" ]
    ParserVersion = "v1.0.0"


}
```