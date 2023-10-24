#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-file-send
  Conditions = [ """"Workload""", """"ResultStatus""", """"Operation""", """"Send""" ]
  ParserVersion = v1.0.0

o365-activity-template = {
  Vendor = Microsoft
  Product = Microsoft 365
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """"CreationTime\\*"+:[\s\\]*"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """\sdvc=({host}\S+)""",
    """\sdvchost=(Unknown|({host}[\w\-.]+))""",
    """"host\\*"+:[\s\\]*"+({host}[^"\\]+)""",
    """\sact=({operation}[^=]+?)\s+(\w+=|$)""",
    """"Operation\\*"+:[\s\\]*"+({operation}[^"\\\.]*)""",
    """"eid\\*"+:[\s\\]*"+(Not Available|SecurityComplianceAlerts|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))\\*"""",
    """UserKey"*:\s*"*({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""",
    """"UserId\\*"+:[\s\\]*"+(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|(Not Available|(({domain}[^"\\\/]+)[\\\/])?(Unknown|((\w+?_)?(\w+-)?\w+-\w+-\w+-\w+)|({user_sid}[^"\\\/@\s]+?))))",""",
    """"MailboxOwnerUPN\\*"+:[\s\\]*"+({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))>?\s*"+""",
    """"(Workload|Application|Client)\\*"+:[\s\\]*"+({app}[^"\\]*)""",
    """sourceServiceName =({app}[^=]+?)\s+(\w+=|$)""",
    """"app"+:\{[^\}]+?"displayName"+:"+({app}[^"]+)"""",
    """"ObjectId\\*"+:"?[\s\\]*"+(Unknown|Not Available|({object}[^"\\]*?))\s*"""",
    """"Client\\*"+:[\s\\]*"+({user_agent}[^"]*)""",
    """"User-?Agent\\*"+:[\s\\]*"(|({user_agent}[^\\"]+))\\*"""",
    """\{"+Name"+:[\s\\]*"+UserAgent"+,"+Value"+:"+({user_agent}[^"]+)"+\}""",
    """"+Value"+:\s*"+({user_agent}[^"]+)"+,\s*"+Name"+:[\s\\]*"+UserAgent"+\},""",
    """"Parameters"+:[\s\\]*\[({additional_info}[^=]+?)\s*\]""",
    """"ExtendedProperties"[^]]*?UserAgent"+,\s*"+Value"+:\s*"+({user_agent}[^"]+)""",
    """"AffectedItems"+:[\s\\]*\[({additional_info}[^=]+?)\s*\],""",
    """"ClientIP\\*"+:[\s\\]*"+\[?((0\.0\.0\.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\]?(:({=src_port}\d+))|((0\.0\.0\.0|({=src_ip}[a-fA-F\d.:]+))\]?(:({=src_port}\d+))?))"""",
    """\ssuser=((Not Available|anonymous|SecurityComplianceAlerts|([^#]+#)?({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|(Unknown|(\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|((({domain}[^\\\s]+)\\)?(S-(\d{1,2}\-){3}(\d+\-){3}\d+|({user}[\w\.\-]{1,40}\$?))))))\s""",
    """"ClientIPAddress\\*"+:[\s\\]*"+\[?(::1|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\]?(:({=src_port}\d+))?""",
    """\sreason=(?:None|({failure_reason}[^\s]+))""",
    """\{"Value": "(?:None|({failure_reason}[^"]+))", "Name": "MethodExecutionResult."\}""",
    """"Path":"(\\+)?(\?+|({object}[^=]+?))\s*"""",
    """"Subject":"\s*({additional_info}[^"]+?)\s*"""",
    """"trc":"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))""",
    """src-account-name":"({account_name}[^"]+)""",
    """"OriginatingServer":"({src_host}[\w\-.]+?)\s*\(""",
    """Workload"*:\s*"*({resource}[^"]+)"""",
    """"Path":"(\\+)?(\?+|({target}[^"\}\]]+?))\s*"""",
    """Recipients":\[?"({target}[^\s,;@"]+@({dest_domain}[^\s;,"]+))""",
    """"ResultStatus":\s*"({result}Success|Succeeded|Failed|Failure)""",
    """"DeviceProperties":\s*\[\{[^\]]+?(("Value":\s*"({src_host}[^"]+)",\s*"Name":\s*"DisplayName")|("Name":\s*"DisplayName",\s*"Value":\s*"({=src_host}[^"]+)"))\},""",
    """"os":"({os}[^"]+)"""",
    """"(browser|BrowserName)":"({browser}[^"]+)""""
    """"ClientInfoString":"({user_agent}[^"]+)","""
  ]
  DupFields = ["operation->event_name"
}
```