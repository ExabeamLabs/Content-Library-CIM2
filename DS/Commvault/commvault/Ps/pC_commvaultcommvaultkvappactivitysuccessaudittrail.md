#### Parser Content
```Java
{
Name = commvault-commvault-kv-app-activity-success-audittrail
    Vendor = "Commvault"
    Product = "Commvault"
    TimeFormat = "dd MMM yyyy HH:mm:ss"
    Conditions = [ """AuditTrail:""", """Commcellname =""", """Operation =""", """Username =""", """Details = {""" ]
    Fields = [
        """Opid\s*=\s*\{({event_id}[\d]+)\}""",
        """Audittime\s*=\s*\{({time}\d+\s+\w+\s+\d+\s+\d+:\d+:\d+)\}""",
        """Severitylevel\s*=\s*\{({severity}[^}]+)\}""",
        """Commcellname\s*=\s*\{({host}[\w\-.]+?)\}""",
        """Username\s*=\s*\{(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))\}""",
        """Operation\s*=\s*\{({action}({operation}[^}]+))\}""",
        """username:\[(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))\],""",
        """host/ device:\[({src_ip}(?:(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.){3}(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?))\]""",
        """logged in from:\s*\[({app}[^\]]+)\]""",
        """Companyname\s*=\s*\{({company}[^}]+)\}""",
        """Client:\s*({client_name}\S+)""",
        """Display Name: Set to\s*\[({resource_name}[^\]]+)\]""",
        """SMTP Address: Set to\s*\[({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\]""",
        """Policy Name: Set to\s*\[({policy_name}[^\]]+)\]""",
        """ Client\s+:\s*\[\{({src_host}[\w\-.]+?)\]""",
        """Agent Type\s*:\s*\[({object_type}[^\]]+)\]""",
        """Application Type:\s*Set to \[({object_type}[^\]]+)\]""",
        """Azure application display name: Set to\s*\[({app}[^\]]+)\]""",
        """Application ID: Set to\s*\[({app_id}[^\]]+)\]""",
        """Azure directory ID: Set to\s*\[({directory_id}[^\]]+)\]""",
        """Accessing entities\s*\[({object_type}[^:]+):[^\]]+\] in client\s*\[({src_host}[\w\-.]+?)\]""",
        """System has created an account with login\s*\[(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\]""",
        """Details\s*=\s*\{.*?Login ({result}[^:]+):"""
        """Client Type:\s*Set to\s*\[({client_type}[^\]]+)\]""",
    ]
    ParserVersion = "v1.0.0"


}
```