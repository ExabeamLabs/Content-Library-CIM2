#### Parser Content
```Java
{
Name = microsoft-o365-cef-app-activity-success-inboxrule
  ParserVersion = v1.0.0
  Product = Office 365
  Conditions= [ """destinationServiceName =Office 365""", """"New-InboxRule"""" ]
  Fields = ${MicrosoftAzureParsersTemplates.cef-microsoft-app-activity-1.Fields}[
    """"(?i)({operation}ForwardTo|delivertomailboxandforward)""""
    """"ForwardTo":"+(smtp:)?({target}[^"]+@({dest_domain}[^"]+))""""
    """"SubjectOrBodyContainsWords":"({filter_key_words}[^"]+)"""
    """"ResultStatus":"({result}[^"]+)"""",
  ]

cef-microsoft-app-activity-1 = {
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """activityDate":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """env_time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"CreationTime\\*"+:[\s\\]*"+({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) [\w\-.]+ """,
    """"OriginatingServer":"({host}\w+)\s*(\([^\)]+?\))?(\\r\\n)?"""",
    """CEF:([^\|"]*\|){5}({operation}[^\|"]+)""",
    """\sflexString1=({operation}[^=]+?)\.?\s+(\w+=|$)""",
    """"Operation":"({operation}[^"]+?)\.?"""",
    """"ObjectId":"(Unknown|Not Available|({object}[^"]+?))\s*"""",
    """\sfname=\s*(N\/A|({object}[^=]+?))\s*(\w+=|$)""",
    """((fileType=(n\/a|N\/A|mail|calendar-event|note|message)[^\n]*?\sfname=\s*(N\/A|({alert_subject}[^=]+?)))|(fileType=group[^\n]*?\sfname=\s*(N\/A|({group_name}[^=]+?)))|(fileType=(file|folder|attachment|report)[^\n]*?\sfname=\s*(N\/A|({file_name}[^=]+?)))|(fileType=process[^\n]*?\sfname=\s*(N\/A|({process_name}[^=]+?)))|(fileType=app(lication)?[^\n]*?\sfname=\s*(N\/A|({app}[^=]+?))))\s+(\w+=|$)""",
    """\Wmsg=({additional_info}[^=]+?)\s+(\w+=|$)""",
    """\ssuser=((\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|(Unknown|Microsoft Intune|Microsoft Teams (Templates )?Service(s)?|Microsoft Online Services|Office 365 (SharePoint|Exchange) Online|anonymous|EMPTY\.*|(\w{1,5}:\w{1,5}:[^\#]+\#)?({email_address}[^@\s"]+@[^@\s\."]+\.[^\s",]+)|(({domain}[^\\\s@]+)\\)?(system|Unknown|({user}[^@\s]+))|(Sync Client|Office365 Backend Process|Device Registration Service|Managed Service Identity|Microsoft Substrate Management|Microsoft Approval Management|Office 365 Exchange Online|Office 365 SharePoint Online|Microsoft Office 365 Portal|Microsoft App Access Panel|Microsoft Invitation Acceptance Portal|Azure ESTS Service|Microsoft B2B Admin Worker|Microsoft Stream Portal|Microsoft Stream Service|Azure AD Cloud Sync|Azure AD PIM|Portfolios|ProjectWorkManagement|AAD Terms Of Use|({full_name}[\w,\s]+?))))\s+(\w+=|$)""",
    """"+UserId"+:"+((\w{1,5}:\w{1,5}:[^\#]+\#)?({email_address}[^@\s"]+?@({email_domain}[^@\s\."]+\.[^\s",]+))|({full_name}({first_name}[^"\s]+)\s({last_name}[^"]+))|(Unknown|({user_sid}[^"]+)))"+""",
    """"ClientIP":"(::1|::ffff:|\[?(::ffff:)?({src_ip}[A-Fa-f:\d.]+?)(\]:({src_port}\d+))?)"""",
    """\ssrc=\[?(::ffff:)?({src_ip}((\d{1,3}\.){3}\d{1,3}|[A-Fa-f\d]+:[a-fA-F\d:]+))\]?(:({src_port}\d+))?\s\w+=""",
    """"result":"({result}[^"]+)""",
    """"ResultStatus":"({result}[^"]+?)"""",
    """\sdestinationServiceName\s*=({app}[^=]+?)\s+(\w+=|$)""",
    """\ssourceServiceName =(Core Directory|Account Provisioning|({app}[^=]+?))\s+(\w+=|$)""",
    """"app"+:\{[^\}]+?"displayName"+:"+({app}[^"]+)"""",
    """"User-Agent\\?"+:\\?"+({user_agent}[^"\\]+)"""
    """"UserAgent":"({user_agent}[^"]+)"""",
    """"ipAddress":"({dest_ip}[A-Fa-f.:\d]+)"""",
    """"SourceFileName":"({src_file_name}[^",]+)"""
    """"user":\{[^}]+?displayName":"(Microsoft Teams Services|({full_name}[^"]+))"""",
    """"resultReason":"({failure_reason}[^"]+?)\s*""""
  
}
```