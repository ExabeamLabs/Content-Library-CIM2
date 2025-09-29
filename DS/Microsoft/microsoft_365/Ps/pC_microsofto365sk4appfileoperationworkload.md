#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-file-operationworkload
  Vendor = Microsoft
  Product = Microsoft 365
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"Workload""", """"ResultStatus""", """"Operation""" ]
  Fields = [
    """"CreationTime\\*"+:[\s\\]*"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """\sdvc=({host}\S+)""",
    """\sdvchost=(Unknown|({host}[\w\-.]+))""",
    """"host\\*"+:[\s\\]*"+({host}[^"\\]+)""",
    """\sact=({operation}[^=]+?)\s+(\w+=|$)""",
    """"Operation\\*"+:[\s\\]*"+({operation}[^"\\\.]*)""",
    """"eid\\*"+:[\s\\]*"+(Not Available|SecurityComplianceAlerts|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\\*"""", 
    """"UserId\\*"+:[\s\\]*"+(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(Not Available|(({domain}[^"\\\/]+)[\\\/])?(Unknown|((\w+?_)?(\w+-)?\w+-\w+-\w+-\w+)|({user_sid}[^"\\\/@\s]+?))))",""",
    """"MailboxOwnerUPN\\*"+:[\s\\]*"+({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))>?\s*"+""",
    """"(Workload|Application|Client)\\*"+:[\s\\]*"+({app}[^"\\]*)""",
    """sourceServiceName =({app}[^=]+?)\s+(\w+=|$)""",
    """"app"+:\{[^\}]+?"displayName"+:"+({app}[^"]+)"""",
    """"ObjectId\\*"+:"?[\s\\]*"+(Unknown|Not Available|({object_id}[^"\\]{0,249}?))\s*"""",
    """"Client\\*"+:[\s\\]*"+({user_agent}[^"]*)""",
    """"(U|u)serAgent\\*"+:[\s\\]*"(|({user_agent}[\s\S]*?))\\*",""",
    """\{"+Name"+:[\s\\]*"+UserAgent"+,"+Value"+:"+({user_agent}[^"]+)"+\}""",
    """"+Value"+:\s*"+({user_agent}[^"]+)"+,\s*"+Name"+:[\s\\]*"+UserAgent"+\},""",
    """"Parameters"+:[\s\\]*\[({additional_info}[^=]+?)\s*\]""",
    """"ExtendedProperties"[^]]*?UserAgent"+,\s*"+Value"+:\s*"+({user_agent}[^"]+)""",
    """"AffectedItems"+:[\s\\]*\[({additional_info}[^=]+?)\s*\],""",
    """"ClientIP\\*"+:[\s\\]*"+\[?(::ffff:)?((({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F:]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\%\d+)?(:({src_port}\d+))?)\]?(:({=src_port}\d+))?)"""",
    """\ssuser=((Not Available|anonymous|SecurityComplianceAlerts|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|(Unknown|(\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|((({domain}[^\\\s]+)\\)?(S-(\d{1,2}\-){3}(\d+\-){3}\d+|({user}[\w\.\-\!\#\^\~]{1,40}\$?))))))\s""",
    """\sreason=(?:None|({failure_reason}[^\s]+))""",
    """\{"Value": "(?:None|({failure_reason}[^"]+))", "Name": "MethodExecutionResult."\}""",
    """"Path":"(\\+)?(\?+|Unknown|Not Available|({object}[^=]+?))\s*"""",
    """"Subject":"\s*({additional_info}[^"]+?)\s*"""",
    """"trc":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """src-account-name":"({account_name}[^"]+)""",
    """"Target"[^\]]+"Device"[^\]]+"ID":"({host}[\w\-.]+)""""
    """"OriginatingServer":"({host}[\w\-.]+?)\s*\(""",
    """Workload"*:\s*"*({resource}[^"]+)"""",
    """"Path":"(\\+)?(\?+|({target}[^"\}\]]+?))\s*"""",
    """Recipients":\[?"({target}[^\s,;@"]+@({dest_domain}[^\s;,"]+))""",
    """"ResultStatus":\s*"({result}Success|Succeeded|Failed|Failure|Dismissed)"""
    """"DeviceProperties":\s*\[\{[^\]]+?(("Value":\s*"({src_host}[^"]+)",\s*"Name":\s*"DisplayName")|("Name":\s*"DisplayName",\s*"Value":\s*"({=src_host}[^"]+)"))\},"""
    """"ApplicationId":({app_id}\d+)""",
    """"ServiceObjectType":"({role_name}[^",\}]+)""",
    """"Target":.+?"ID":"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)"""",
    """("Device\.DisplayName"[^\}]*?"NewValue":"({src_host}[\w\-\.]+)",)|("NewValue":"({=src_host}[\w\-\.]+)",[^\}]*?"Device\.DisplayName")""",
    """"FileName":"({file_name}[^"]+?(\.({file_ext}[^"\s\.]+))?)"""",
    """"User-Agent\\*"+:[\s\\]*"(|({user_agent}[^=]*?))\\*"""",
    """"os":"({os}[^"]+)"""",
    """"(browser|BrowserName)":"({browser}[^"]+)"""",
    """sourceDnsDomain=({domain}[^=\s]+?)\s\w+="""
    """"UserType":"*\s*({user_type}[^,}"]+)"*"""
    """"LogonError":\s*"({failure_reason}[^"]+)""""
    """"SessionID":\s*"({session_id}[^"]+)""""
    """"ClientProcessName":\s*"({process_name}[^"]+)"""
    """"ClientInfoString":\s*"({user_agent}[^"]+)","""
    """"ActorInfoString":\s*"({user_agent}[^"]+)","""
    """MailboxOwnerUPN":\s"({user_upn}[^"]+)",""",
    """ClientIPAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F:]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """"UserId":\s*"({user_upn}[^",]+)""""
    """"SizeInBytes":\s*({bytes_in}\d+)"""
    """"correlationId":\s*"({correlation_id}[^"]+)""""
    """AlertSeverity":"+({alert_severity}[^"]+)"""
    """"InternalLogonType":({login_type}\d+)"""
    """"LogonType":({login_type}\d+)"""
    """exa_regex="Target"[^\]]+"Device"[^\]]+"ID":"({host}[\w\-.]+)"""
    """exa_regex="Target":.+?"ID":"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)"""
    """exa_regex="User-Agent\\*"+:[\s\\]*"(|({user_agent}[^=]*?))\\*""""
    """exa_regex="FileName":"({file_name}[^"]+?(\.({file_ext}[^"\s\.]+))?)""""
    """exa_json_path=$.CreationTime,exa_field_name=time"""
    """exa_json_path=$.Operation,exa_field_name=operation"""
    """exa_json_path=$.OrganizationId,exa_field_name=tenant_id"""
    """exa_json_path=$.RecordType,exa_field_name=object_type"""
    """exa_json_path=$.UserId,exa_field_name=user_upn"""
    """exa_json_path=$.UserId,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
    """exa_json_path=$.Workload,exa_field_name=app"""
    """exa_json_path=$.Workload,exa_field_name=resource"""
    """exa_json_path=$.MailboxOwnerUPN,exa_regex=^({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))$""",
    """exa_json_path=$.ObjectId,exa_field_name=object_id"""
    """exa_json_path=$.ExtendedProperties,exa_field_name=more_info"""
    """exa_json_path=$.ClientIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.ClientIPAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.OriginatingServer,exa_regex=({host}[\w\-.]+)"""
    """exa_json_path=$.ResultStatus,exa_field_name=result"""
    """exa_json_path=$.SessionId,exa_field_name=session_id"""
    """exa_json_path=$.ClientProcessName,exa_field_name=process_name"""
    """exa_json_path=$.ClientInfoString,exa_field_name=user_agent""",
    """exa_json_path=$.ActorInfoString,exa_field_name=user_agent""",
    """exa_json_path=$.InternalLogonType,exa_field_name=login_type""",
    """exa_json_path=$.LogonType,exa_field_name=login_type"""
    """exa_json_path=$.OrganizationName,exa_field_name=company"""
    """exa_json_path=$.UserType,exa_field_name=user_type"""
  ]
  DupFields = ["operation->event_name"]
  ParserVersion = "v1.0.0"


}
```