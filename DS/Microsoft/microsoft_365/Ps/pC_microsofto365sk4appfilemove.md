#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-file-move
  ExtractionType = json
  Conditions = [ """"Workload""", """"ResultStatus""", """"Operation""", """"Move""" ]
  ParserVersion = v1.0.0
  Fields = ${MicrosoftAzureParsersTemplates.o365-activity-template.Fields} [
    """exa_json_path=$.CreationTime,exa_field_name=time""",
    """exa_json_path=$.Operation,exa_field_name=operation""",
    """exa_json_path=$.UserId,exa_field_name=user_upn""",
    """exa_json_path=$.MailboxOwnerUPN,exa_regex=^({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))$""",
    """exa_json_path=$.Workload,exa_field_name=app""",
    """exa_json_path=$.ClientIP,exa_regex=^\[?((0\.0\.0\.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\]?(:({=src_port}\d+))|((0\.0\.0\.0|({=src_ip}[a-fA-F\d.:]+))\]?(:({=src_port}\d+))?))$""",
    """exa_json_path=$.ClientIPAddress,exa_regex=^\[?(::1|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\]?(:({=src_port}\d+))?$""",
    """exa_json_path=$.Item.ParentFolder.Name,exa_field_name=object""",
    """exa_json_path=$.OriginatingServer,exa_regex=({host}[\w\-.]+?)\s*\(""",
    """exa_json_path=$.Workload,exa_field_name=resource""",
    """exa_json_path=$.Item.ParentFolder.Path,exa_regex=^(\\+)?(\?+|({target}[^"\}\]]+?))$""",
    """exa_json_path=$.ResultStatus,exa_field_name=result""",
    """exa_json_path=$.ClientInfoString,exa_field_name=user_agent""",
    """exa_json_path=$.ActorInfoString,exa_field_name=user_agent""",
    """exa_json_path=$.UserType,exa_field_name=user_type""",
    """exa_json_path=$.OperationProperties[?(@.Name == 'RuleName')].Value,exa_field_name=rule"""
  ]

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
    """"eid\\*"+:[\s\\]*"+(Not Available|SecurityComplianceAlerts|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\\*"""", 
    """"UserId\\*"+:[\s\\]*"+({user_upn}[^",]+)",""",
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
    """"ClientIP\\*"+:[\s\\]*"+\[?((0\.0\.0\.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\]?(:({=src_port}\d+))?|((0\.0\.0\.0|({=src_ip}[a-fA-F\d.:]+))\]?(:({=src_port}\d+))?))"""",
    """\ssuser=((Not Available|anonymous|SecurityComplianceAlerts|([^#]+#)?({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|(Unknown|(\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|((({domain}[^\\\s]+)\\)?(S-(\d{1,2}\-){3}(\d+\-){3}\d+|({user}[\w\.\-\!\#\^\~]{1,40}\$?))))))\s""",
    """"ClientIPAddress\\*"+:[\s\\]*"+\[?(::1|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\]?(:({=src_port}\d+))?""",
    """\sreason=(?:None|({failure_reason}[^\s]+))""",
    """\{"Value": "(?:None|({failure_reason}[^"]+))", "Name": "MethodExecutionResult."\}""",
    """"Path":"(\\+)?(\?+|({object}[^=]+?))\s*"""",
    """"Subject":"\s*({additional_info}[^"]+?)\s*"""",
    """"trc":"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))""",
    """src-account-name":"({account_name}[^"]+)""",
    """"OriginatingServer":"({host}[\w\-.]+?)\s*\(""",
    """Workload"*:\s*"*({resource}[^"]+)"""",
    """"Path":"(\\+)?(\?+|({target}[^"\}\]]+?))\s*"""",
    """Recipients":\[?"({target}[^\s,;@"]+@({dest_domain}[^\s;,"]+))""",
    """"ResultStatus":\s*"({result}Success|Succeeded|Failed|Failure)""",
    """"DeviceProperties":\s*\[\{[^\]]+?(("Value":\s*"({src_host}[^"]+)",\s*"Name":\s*"DisplayName")|("Name":\s*"DisplayName",\s*"Value":\s*"({=src_host}[^"]+)"))\},""",
    """"os":"({os}[^"]+)"""",
    """"(browser|BrowserName)":"({browser}[^"]+)""""
    """"ClientInfoString":"({user_agent}[^"]+)","""
    """"ActorInfoString":"({user_agent}[^"]+)","""
    """"UserType":\s*"*({user_type}[^,}"]+)"*"""
    """"correlationId":\s*"({correlation_id}[^"]+)""""
  ]
  DupFields = ["operation->event_name"
}
```