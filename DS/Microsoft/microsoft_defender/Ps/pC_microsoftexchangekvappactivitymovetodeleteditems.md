#### Parser Content
```Java
{
Name = "microsoft-exchange-kv-app-activity-movetodeleteditems"
Conditions = [ """WORKLOAD=Exchange""", """COMMAND=MoveToDeletedItems""", """CLIENTPROCESSNAME=""", """TS=""" ]
ParserVersion = "v1.0.0"

cef-microsoft-app-activity-3.Fields}[
    """({user_upn}claims/upn)""",
    """eventName":"({event_name}[^"]+)""""
    """"resultType":"({result}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"
}

{
  Name = microsoft-defendercloud-json-alert-trigger-success-assessments
  Vendor = Microsoft
  Product = Microsoft Defender
  ExtractionType = json
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSZ" ]
  Conditions= [ """"type":"Microsoft.Security/assessments""", """"action":"""", """"id":""", """"properties":""" ]
  Fields =[
    """exa_json_path=$.properties.timeGenerated,exa_field_name=time""",
    """exa_json_path=$.properties.resourceDetails.resourceName,exa_field_name=src_host""",
    """exa_json_path=$.properties.resourceDetails.resourceType,exa_field_name=resource_type""",
    """exa_json_path=$.properties.resourceDetails.source,exa_field_name=alert_source""",
    """exa_json_path=$.properties.resourceDetails.id,exa_field_name=resource_path""",
    """exa_json_path=$.properties.displayName,exa_field_name=alert_subject""",
    """exa_json_path=$.properties.description,exa_field_name=additional_info""",
    """exa_json_path=$.properties.impact,exa_field_name=impact""",
    """exa_json_path=$.properties.remediation,exa_field_name=remediation_steps""",
    """exa_json_path=$.properties.category,exa_field_name=category""",
    """exa_json_path=$.properties.status.severity,exa_field_name=alert_severity""",
    """exa_json_path=$.properties.additionalData.query,exa_field_name=query_string""",
    """exa_json_path=$.properties.additionalData.assessedResourceType,exa_field_name=azure_resource_type""",
    """exa_json_path=$.properties.additionalData.scanId,exa_field_name=scan_id""",
    """exa_json_path=$.properties.category,exa_field_name=scan_type""",
    """exa_json_path=$.type,exa_field_name=alert_type""",
    """exa_json_path=$.type,exa_field_name=alert_name""",
    """exa_json_path=$.properties.category,exa_field_name=alert_name""",
    """exa_json_path=$.tenantId,exa_field_name=tenant_id"""
  ]
  DupFields = [ "src_host->resource_name" ]
  ParserVersion = v1.0.0
}

]

#============================================== End of MicrosoftAzureParsers section ==================================================================
#============================================== Start of MicrosoftAzureParsersDL section ==================================================================
MicrosoftAzureParsersDL = [
{
Name = "microsoft-exchange-sk4-app-activity-success-harddelete"
Vendor = "Microsoft"
Product = "Microsoft Exchange"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [  """destinationServiceName =Office 365""", """flexString1=HardDelete """, """request=Success""" ]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+\w)"""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wsuser=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(\w+=|$)"""
  """\Wfname=({object}.+?)\s+(\w+=|$)"""
  """\WsourceServiceName =({app}.+?)\s+(\w+=|$)"""
  """\WflexString1=({operation}.+?)\s+(\w+=|$)"""
  """\Wmsg=({additional_info}.+?)\s+(\w+=|$)"""
  """destinationServiceName =({event_subtype}.+?)\s+(\w+=|$)"""
]
DupFields = [
  "user->email_address"
]
ParserVersion = "v1.0.0"
},

{
Vendor = "Microsoft"
Product = "Microsoft Exchange"
TimeFormat = "epoch"
Fields = [
  """\Wdvc=({host}\S+)"""
  """\Wdvchost=({host}[\w\-.]+)"""
  """\Wact=({operation}.+?)\s+(\w+=|$)"""
  """\Wrt=({time}\d{13})"""
  """\Wduser=({email_address}[^@\s]+@({email_domain}[^\s@]+))"""
  """\Wsuser=({email_address}[^@\s]+@({email_domain}[^\s@]+))"""
  """\Wsuid=({email_address}[^@\s]+@({email_domain}[^\s@]+))"""
  """\Woutcome=({result}.+?)\s+(\w+=|$)"""
  """CEF:([^\|]*\|){2}({app}[^\|]+)"""
  """cs3=({email_subject}[^=]+?)\s*((\w+=)|$)"""
  """cn1=({login_type}\d+)"""  
]
Name = "microsoft-exchange-cef-app-activity-movetodeleteditems"
Conditions = [ """CEF:""", """|Exchange Online|""", """|MoveToDeletedItems|""" ]
ParserVersion = "v1.0.0"
},

{
Vendor = "Microsoft"
Product = "Microsoft Exchange"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Fields = [
  """TS=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """WORKLOAD=({app}[^\s]+)"""
  """USER=(({email_address}[^@\s]+@({email_domain}[^\s@]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """SIP=\[*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\]*(:({src_port}\d+))?"""
  """ORIGINATINGSERVER=({host}[^\s]+)"""
  """LOGONUSERSID=({user_sid}[^\s]+)"""
  """COMMAND=({operation}[^\s]+)"""
  """RESULTCODE=({result}[^\s]+)"""
  """CLIENTPROCESSNAME=({process_path}[^\s]+)"""
  """Path\":\"({path}[^\"]+?)\s*\""""
  """\"Subject\":\"\s*({email_subject}[^\"}]+?)\s*\""""
  """\"Attachments\\*\"+:[\s\\]*\"+\s*({email_attachments}[^\"\\]+)\s*"""
  """\"Attachments\\*\"+:[\s\\]*\"+\s*({attachment}[^\"\\;]+)\s*"""
  """SESSID=({message_id}[^\s]+)"""
]
Name = "microsoft-exchange-kv-app-activity-harddelete"
Conditions = [ """WORKLOAD=Exchange""", """COMMAND=HardDelete""", """CLIENTPROCESSNAME=""", """TS=""" ]
ParserVersion = "v1.0.0"
},

{
Vendor = "Microsoft"
Product = "Microsoft Exchange"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Fields = [
  """TS=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """WORKLOAD=({app}[^\s]+)"""
  """USER=(({email_address}[^@\s]+@({email_domain}[^\s@]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """SIP=\[*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\]*(:({src_port}\d+))?"""
  """ORIGINATINGSERVER=({host}[^\s]+)"""
  """LOGONUSERSID=({user_sid}[^\s]+)"""
  """COMMAND=({operation}[^\s]+)"""
  """RESULTCODE=({result}[^\s]+)"""
  """CLIENTPROCESSNAME=({process_path}[^\s]+)"""
  """Path\":\"({path}[^\"]+?)\s*\""""
  """\"Subject\":\"\s*({email_subject}[^\"}]+?)\s*\""""
  """\"Attachments\\*\"+:[\s\\]*\"+\s*({email_attachments}[^\"\\]+)\s*"""
  """\"Attachments\\*\"+:[\s\\]*\"+\s*({attachment}[^\"\\;]+)\s*"""
  """SESSID=({message_id}[^\s]+)"""
  """"ParentFolder":[^=]+?"Path":"\\*({object}[^"]+)""""
  """"Subject":"({email_subject}[^"]+?)\s*""""
]
Name = "microsoft-exchange-kv-app-activity-movetodeleteditems"
Conditions = [ """WORKLOAD=Exchange""", """COMMAND=MoveToDeletedItems""", """CLIENTPROCESSNAME=""", """TS=""" ]
ParserVersion = "v1.0.0"
},

{
Vendor = "Microsoft"
Product = "Microsoft Exchange"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Fields = [
"""TS=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""WORKLOAD=({app}[^\s]+)"""
"""USER=(({email_address}[^@\s]+@({email_domain}[^\s@]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""SIP=\[*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\]*(:({src_port}\d+))?"""
"""ORIGINATINGSERVER=({host}[^\s]+)"""
"""LOGONUSERSID=({user_sid}[^\s]+)"""
"""COMMAND=({operation}[^\s]+)"""
"""RESULTCODE=({result}[^\s]+)"""
"""CLIENTPROCESSNAME=({process_name}[^\s]+)"""
"""Path":"({process_path}[^"]+?)\s*""""
""""Subject":"\s*({email_subject}[^"}]+?)\s*""""
""""Attachments\\*"+:[\s\\]*"+\s*({email_attachments}[^"\\]+)\s*"""
""""Attachments\\*"+:[\s\\]*"+\s*({attachment}[^"\\;]+)\s*"""
"""SESSID=({message_id}[^\s]+)"""
"""InternetMessageId":"({message_id}[^"]+)""""
"""LOGONTYPE=({login_type}\d+)"""
""""ParentFolder":[^=]+?"Path":"\\*({object}[^"]+)"""",
""""Subject":"({email_subject}[^"]+?)\s*""""
]
Name = "microsoft-exchange-kv-app-activity-softdelete"
Conditions = [
"""WORKLOAD=Exchange"""
"""COMMAND=SoftDelete"""
"""CLIENTPROCESSNAME="""
"""TS="""
]
ParserVersion = "v1.0.0"
},

{
Vendor = "Microsoft"
Product = "Microsoft Exchange"
TimeFormat = "epoch"
Fields = [
  """\Wdvc=({host}\S+)"""
  """\Wdvchost=({host}[\w\-.]+)"""
  """\Wact=({operation}.+?)\s+(\w+=|$)"""
  """\Wrt=({time}\d{13})"""
  """\Wduser=({email_address}[^@\s]+@({email_domain}[^\s@]+))"""
  """\Wsuser=({email_address}[^@\s]+@({email_domain}[^\s@]+))"""
  """\Wsuid=({email_address}[^@\s]+@({email_domain}[^\s@]+))"""
  """\Woutcome=({result}.+?)\s+(\w+=|$)"""
  """CEF:([^\|]*\|){2}({app}[^\|]+)"""
  """\Wcat=({category}.+?)\s+(\w+=|$)"""
  """\Wsproc=({process_name}.+?)\s*(\w+=|$)"""
  """\Wcs3=({email_subject}.+?)\s*(\w+=|$)"""
]
Name = "microsoft-exchange-cef-app-activity-softdelete"
Conditions = [ """CEF:""", """|Exchange Online|""", """|SoftDelete|""" ]
ParserVersion = "v1.0.0"
},

{
  Name = microsoft-azuremon-sk4-http-session-appservicehttplogs
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  ParserVersion = v1.0.0
  Conditions = [ """"resourceId":""", """"category":""", """"AppServiceHTTPLogs"""" ]
  Fields = [
    """"time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """([^\|]*\|){5}({operation}[^\|]+)""",
    """destinationServiceName =({app}.+?)\s+(\w+=|$)""",
    """\Wsuser=(anonymous|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+[\S]+=|\s*$)""",
    """\Wsuid=(anonymous|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+[\S]+=|\s*$)""",
    """"CsHost\\?":\\?"({app}[^:",]+?)\\?"""",
    """"Result\\?":\\?"({action}[^"]+?)\\?"""",
    """"resourceId":\s*"({resource}[^"]+)"""",
    """"CsUriStem\\?":\\?"({uri_path}[^"]+?)\\?"""",
    """"CIp\\?":\\?"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\\?"""",
    """"UserAgent\\?":\\?"(-|({user_agent}[^"]+?))\\?"""",
    """"category":\s*"({category}[^"]+)"""",
    """"CsMethod\\?":\\?"({method}[^"]+?)\\?"""",
    """"SPort\\?":\\?"({src_port}\d+)\\?"""",
    """"CsUriQuery\\?":\\?"(-|({uri_query}[^"]+?))\\?"""",
    """"CsBytes\\?":\\?"*({bytes_in}\d+)\\?"*,""",
    """"CsUsername\\?":\\?"(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?"""",
    """"Referer\\?":\\?"(-|({referrer}[^"]+?))\\?"""",
    """"ScBytes\\?":\\?"*({bytes_out}\d+)\\?"*,""",
    """"ScStatus\\?":\\?"*({http_response_code}\d+)\\?"*,""",
    """\[Namespace:\s*({event_hub_namespace}\S+) ; EventHub name:\s*({event_hub_name}[\w-]+)""",
    """"UserAgent\\?":\\?"(?:-|Mozilla\/[^"]+?({os}iOS|Android|BlackBerry|Windows Phone|BeOS|(?:X|x)11|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin).+?({browser}Chrome|Safari|Opera|(?:F|f)irefox|MSIE|Trident))"""
  ]
  DupFields = ["app->web_domain", "event_hub_namespace->host"
}
```