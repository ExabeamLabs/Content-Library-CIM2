#### Parser Content
```Java
{
Name = cyberark-pam-str-user-switch-success-retrievepassword
    Vendor = CyberArk
    Product = "CyberArk Privilege Access Manager"
    TimeFormat = ["yyyy-MM-dd HH:mm:ss","MMM dd HH:mm:ss"]
    Conditions = [ """Operation: Retrieve Password ObjectType:""" ]
    Fields = [
        """Operation: ({operation}.*?) ObjectType""",
  """({time}(\w+\s+\d\d\s+\d\d:\d\d:\d\d))[^:]+:\s+(AdminName|UserName)"""
	"""({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
	"""(AdminName|UserName):\s({user}[\w\.\-]{1,40}\$?)\sOperation""",
	"""Target:\s*(?:({account_domain}[^\\\/]+)[\\\/]+)?({dest_user}.+?)\s*Role:""",
	""":\d\d\s({host}[^=]+)\sPAR""",
	"""PAR\[({event_code}\d+)"""
    ]
    DupFields = [ "host->dest_host", "dest_user->account", "dest_domain->account_domain" ]
    ParserVersion = "v1.0.0"


}
```