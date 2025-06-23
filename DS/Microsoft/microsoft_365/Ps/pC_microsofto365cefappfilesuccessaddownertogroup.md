#### Parser Content
```Java
{
Name = microsoft-o365-cef-app-file-success-addownertogroup
  ParserVersion = v1.0.0
  Product = Microsoft 365
  Conditions= [ """destinationServiceName =Office 365""", """"Add owner to group""" ]
  Fields = ${MSParsersTemplates.cef-microsoft-app-activity.Fields} [
    """sourceServiceName =({app}[^=]+?)\s+(\w+=|$)""",
    """"targetResources":[^\}]+?"displayName":"\s*({target}[^"]+?)\s*""""
  ]

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
    """CEF:([^\|"]*\|){5}({operation}[^\|"]+)""",
    """\sflexString1=({event_name}[^=]+?)\.?\s+(\w+=|$)""",
    """"activityDisplayName":\s*"({operation}[^"]+)""""
    """"resourceId":\s*"({resource_id}[^"]{1,249})""",
    """"Operation":\s*"({operation}[^"]+?)\.?"""",
    """((fileType=(n\/a|N\/A|mail|calendar-event|note|message)[^\n]*?\sfname=\s*(N\/A|({email_subject}[^=]+?)))|(fileType=group[^\n]*?\sfname=\s*(N\/A|({group_name}[^=]+?)))|(fileType=(file|folder|attachment|report)[^\n]*?\sfname=\s*(N\/A|({file_name}[^=]+?)))|(fileType=process[^\n]*?\sfname=\s*(N\/A|({process_name}[^=]+?)))|(fileType=app(lication)?[^\n]*?\sfname=\s*(N\/A|({app}[^=]+?)))|(fileType=secret[^\n]*?\sfname=\s*(N\/A|({secret}[^=]+?)))|(fileType=key[^\n]*?\sfname=\s*(N\/A|({key_name}[^=]+?))))\s+(\w+=|$)""",
    """\Wmsg=({additional_info}[^=]+?)\s+(\w+=|$)""",
    """"initiatedBy".+?\"userPrincipalName\":\"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^"]+))""",
    """\ssuser=((\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|(Unknown|Microsoft Intune|Microsoft Teams (Templates )?Service(s)?|Microsoft Online Services|Office 365 (SharePoint|Exchange) Online|anonymous|EMPTY\.*|(\w{1,5}:\w{1,5}:[^\#]+\#)?({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\\s@]+)\\)?(system|Unknown|({user}[\w\.\-\!\#\^\~]{1,40}\$?))|(Sync Client|Office365 Backend Process|Device Registration Service|Managed Service Identity|Microsoft Substrate Management|Microsoft Approval Management|Office 365 Exchange Online|Office 365 SharePoint Online|Microsoft Office 365 Portal|Microsoft App Access Panel|Microsoft Invitation Acceptance Portal|Azure ESTS Service|Microsoft B2B Admin Worker|Microsoft Stream Portal|Microsoft Stream Service|Azure AD Cloud Sync|Azure AD PIM|Portfolios|ProjectWorkManagement|AAD Terms Of Use|({full_name}[\w,\s]+?))))\s+(\w+=|$)""",
    """"+UserId"+:"+((\w{1,5}:\w{1,5}:[^\#]+\#)?({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({full_name}({first_name}[^"\s]+)\s({last_name}[^"]+))|(Unknown|(({user_sid}S-[^\"]+)|({user_id}[^\"]+))))"+""",
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
    """Workload"*:\s*"*({app}[^"]+)"*\}"""
    """destinationServiceName\s*=({app}[^=]+?)\s+(\w+=|$)""",
    """\ssourceServiceName =(Core Directory|Account Provisioning|({app}[^=]+?))\s+(\w+=|$)""",
    """"User-Agent\\?"+:\\?"+({user_agent}[^"\\]+)"""
    """"UserAgent":\s*"({user_agent}[^"]+)"""",
    """("key":\s*"User-Agent","value":\s*"({user_agent}[^"]+?)"|"value":"({=user_agent}[^"]+?)","key":"User-Agent")""",
    """"ipAddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"SourceFileName":"({src_file_name}[^"]+)""""
    """"user":\{[^}]+?displayName":"(Microsoft Teams Services|({full_name}[^"]+))"""",
    """"result":\s*"failure"[^\}]+?"resultReason":\s*"({failure_reason}[^"]+?)\s*",""""
    """"ClientProcessName":\s*"({process_name}[^"]+)"""
    """"ObjectId":\s*"({file_path}({file_dir}[^"]+[\\\/])({file_name}[^"]+?(\.(?!(_|-|\{))({file_ext}[^\\\.\s)"]+))?))""""
    """"UserType":\s*"*\s*({user_type}[^,}"]+)"*"""
    """"(os|Platform)":\s*"({os}[^"]+)""""
    """"(browser|BrowserName)":\s*"({browser}[^"]+)""""
    """"operationType":\s*"({operation_type}[^"]+)"""
    """"loggedByService":\s*"({service_name}[^"]+)""""
    """"category":\s*"({category}[^"]+)"""
    """"Platform":\s*"({os}[^"]+)""""
    """"ClientInfoString":\s*"({user_agent}[^"]+)","""
    """duser=(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """"CorrelationId":\s*"({correlation_id}[^"]+)""""
    """"Application":\s*"({app}[^"]+)"""
    """"type":\s*"User","userPrincipalName":\s*"({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))""",
    """"app"+:[^\]]+?"+displayName"+:"+({app}[^,"]+)"""
    """appId":"({app_id}[^"]+)""""
 
}
```