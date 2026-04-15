#### Parser Content
```Java
{
Name = microsoft-o365-cef-app-file-success-viewdashboard
  ParserVersion = v1.0.0
  Product = Microsoft 365
  Conditions= [ """"Operation":"ViewDashboard"""", """"Workload":""" ]

cef-microsoft-app-activity-2 = {
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) [\w\-.]+ """,
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
    """"Host":"({host}[^"]+)"""",
    """"message":"({additional_info}[^"]+)""",
    """"description":"({additional_info}[^"]+)""",
    """category":"({category}[^"]+)"""",
    """Namespace:\s*(|({event_hub_namespace}[^\]]+?))\s*[\];]""",
    """EventHub name:\s*(|({event_hub_name}[^\]]+?))\s*\]""",
    """resourceId":\s*"({resource}({object}[^"]+))""",
    """"Operation":\s*"({operation}[^"]+)""",
    """"operationName":"({operation}[^"]+)""",
    """"name":"({full_name}[^"]+)"""",
    """action":"({action}[^"]+)""",
    """"(callerIpAddress|CIp)":"({src_ip}((\d{1,3}\.){3}\d{1,3}|[A-Fa-f\d]+:[a-fA-F\d:]+))(:({src_port}\d+))?"""",
    """claims\/(name|upn)":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)""",
    """"email":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)""",
    """({app}Databricks)""",
    """"serviceName\\*":\\*"({app}[^"]+)""",
    """destinationServiceName =({app}[^=]+)\s+(\w+=|$)""",
# port is removed
    """"userAgent":"({user_agent}[^"]+)"""",
    """"statusCode\\":({http_response_code}\d+)""",
    """"actionName":"({operation}[^"]+)""",
    """userId":"({user_upn}[^",]+)""",
    """\[Namespace:\s*({host}\S+) ; EventHub name:"""
    """"UserType":"*({user_type}[^,}"]+)"*"""
    """"Platform":"({os}[^"]+)""""
    """"OriginatingServer":"({host}\w+)\s*(\([^\)]+?\))?(\\r\\n)?""""
    """"ClientInfoString":"({user_agent}[^"]+)","""
    """"ActorInfoString":"({user_agent}[^"]+)","""
    """"BrowserName":"({browser}[^"]+)"""
    """"(Client|Source)IPAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\%\d+)?(:({src_port}\d+))?""""
    """"Workload":\s*"({app}[^"]+)""""
    #"""duser=(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """"CorrelationId":\s*"({correlation_id}[^"]+)""""
    """"TenantId":\s*"({tenant_id}[^"]+)""""
  cef-microsoft-app-activity = {
  Vendor = Microsoft
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ","yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSZ"]
    Fields = [  
    """"activityDateTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """"activityDateTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,7})?Z)"""
    """activityDate":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """env_time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"CreationTime\\*"+:[\s\\]*"+({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
    """"CreationTime\\*"+:[\s\\]*"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) [\w\-.]+ """,
    """"OriginatingServer":(\s*|)"({host}\w+)\s*(\([^\)]+?\))?(\\r\\n)?"""",
    """CEF:([^\|"]*\|){5}({event_name}({operation}[^\|"]+))""",
    """\sflexString1=({event_name}[^=]+?)\.?\s+(\w+=|$)""",
    """"activityDisplayName":\s*"({event_name}({operation}[^"]+))""""
    """"resourceId":\s*"({resource_id}[^"]{1,249})""",
    """"Operation":\s*"({event_name}({operation}[^"]+?))\.?"""",
    """((fileType=(n\/a|N\/A|mail|calendar-event|note|message)[^\n]*?\sfname=\s*(N\/A|({email_subject}[^=]+?)))|(fileType=group[^\n]*?\sfname=\s*(N\/A|({group_name}[^=]+?)))|(fileType=(file|folder|attachment|report)[^\n]*?\sfname=\s*(N\/A|({file_name}[^=]+?)))|(fileType=process[^\n]*?\sfname=\s*(N\/A|({process_name}[^=]+?)))|(fileType=app(lication)?[^\n]*?\sfname=\s*(N\/A|({app}[^=]+?)))|(fileType=secret[^\n]*?\sfname=\s*(N\/A|({secret}[^=]+?)))|(fileType=key[^\n]*?\sfname=\s*(N\/A|({key_name}[^=]+?))))\s+(\w+=|$)""",
    """\Wmsg=({additional_info}[^=]+?)\s+(\w+=|$)""",
    """"initiatedBy".+?\"userPrincipalName\":\"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^"]+))""",
    """\ssuser=((\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|(Unknown|Microsoft Intune|Microsoft Teams (Templates )?Service(s)?|Microsoft Online Services|Office 365 (SharePoint|Exchange) Online|anonymous|EMPTY\.*|(\w{1,5}:\w{1,5}:[^\#]+\#)?({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\\s@]+)\\)?(system|Unknown|({user}[\w\.\-\!\#\^\~]{1,40}\$?))|(Sync Client|Office365 Backend Process|Device Registration Service|Managed Service Identity|Microsoft Substrate Management|Microsoft Approval Management|Office 365 Exchange Online|Office 365 SharePoint Online|Microsoft Office 365 Portal|Microsoft App Access Panel|Microsoft Invitation Acceptance Portal|Azure ESTS Service|Microsoft B2B Admin Worker|Microsoft Stream Portal|Microsoft Stream Service|Azure AD Cloud Sync|Azure AD PIM|Portfolios|ProjectWorkManagement|AAD Terms Of Use|({full_name}[\w,\s]+?))))\s+(\w+=|$)""",
    """"+UserId"+:"+((\w{1,5}:\w{1,5}:[^\#]+\#)?({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({full_name}({first_name}[^"\s]+)\s({last_name}[^"]+))|(Unknown|(({user_sid}S-[^\"]+)|({user_id}[^\"]+))))"+""",
    """"ClientIP":"(::1|::ffff:|\[?(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)(\%\d+)?(\]:({src_port}\d+))?)"""",
    """\ssrc=\[?(::ffff:)?({src_ip}((\d{1,3}\.){3}\d{1,3}|[A-Fa-f\d]+:[a-fA-F\d:]+))\]?(:({src_port}\d+))?\s\w+=""",
    """"ObjectId"*:\s*"*(null|({object}[^"]+))"*""",
    """DatasetName"*:\s*"*({file_name}[^"]+)"""
    """Workload"*:\s*"*({resource}[^"]+)"*"""
    """"activityResultStatus":"({result}[^"]+?)"""",
    """"IsSuccess":\s*({result}[\w]+)"""
    """"result":\s*"\s*({result}[^"]+)""",
    """"ResultStatus":\s*"({result}[^"]+?)"""",
    """Workload"*:\s*"*({app}[^"]+)""",
    """Workload"*:\s*"*({app}[^"]+)"*\}
}
```