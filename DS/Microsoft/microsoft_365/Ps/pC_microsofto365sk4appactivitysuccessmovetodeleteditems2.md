#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-activity-success-movetodeleteditems-2
  ParserVersion = v1.0.0
  Product = Microsoft 365
  Conditions= [ """"Workload":""", """"Operation":"MoveToDeletedItems"""", """"UserId":"""" ]
  Fields = ${MicrosoftAzureParsersTemplates.cef-microsoft-o365-app-activity-1.Fields} [
    """\WfilePath=(((?i)N\/A)|({file_path}[^=]+?))\s*(\w+=|$)""",
    """\WfilePath=(((?i)N\/A)|(({file_dir}[^=]+?)\/({file_name}[^\/=]+?(\.({file_ext}[^\/=\.\s]+?))?)))\s*(\w+=|$)""",
    """\sfname=\s*(N\/A|({object}[^=\s]+))""",
    """\ssourceServiceName =(Core Directory|Account Provisioning|({app}[^=]+?))\s+(\w+=|$)""",
    """"Folder":\{[^\}]*?"Path":"([^"]*\\+)?({folder_name}[^"]+)""""
  ]

cef-microsoft-o365-app-activity-1 = {
  Vendor = Microsoft
  Product = Microsoft 365
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """"CreationTime\\*"+:[\s\\]*"+({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
    """"OriginatingServer":"({host}\w+)\s*(\([^\)]+?\))?(\\r\\n)?"""",
    """CEF:([^\|"]*\|){5}({operation}[^\|"]+)""",
    """\sflexString1=({event_name}[^=]+?)\.?\s+(\w+=|$)""",
    """"Operation":"({operation}[^"]+?)\.?"""",
    """\sfname=\s*(N\/A|({object}[^=\s]+))""",
    """((fileType=(n\/a|N\/A|mail|calendar-event|note|message)[^\n]*?\sfname=\s*(N\/A|({email_subject}[^=]+?)))|(fileType=group[^\n]*?\sfname=\s*(N\/A|({group_name}[^=]+?)))|(fileType=(file|folder|attachment|report)[^\n]*?\sfname=\s*(N\/A|({file_name}[^=]+?)))|(fileType=process[^\n]*?\sfname=\s*(N\/A|({process_name}[^=]+?)))|(fileType=app(lication)?[^\n]*?\sfname=\s*(N\/A|({app}[^=]+?))))\s+(\w+=|$)""",
    """\Wmsg=({additional_info}[^=]+?)\s+(\w+=|$)""",
    """\ssuser=((\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|(Unknown|Microsoft Intune|Microsoft Teams (Templates )?Service(s)?|Microsoft Online Services|Office 365 (SharePoint|Exchange) Online|anonymous|EMPTY\.*|(\w{1,5}:\w{1,5}:[^\#]+\#)?({email_address}[^@\s"]+@[^@\s\."]+\.[^\s",]+)|(({domain}[^\\\s@]+)\\)?(system|Unknown|Signup|({user}[\w\.\-\!\#\^\~]{1,40}\$?))|(Sync Client|Office365 Backend Process|Device Registration Service|Managed Service Identity|Microsoft Substrate Management|Microsoft Approval Management|Office 365 Exchange Online|Office 365 SharePoint Online|Microsoft Office 365 Portal|Microsoft App Access Panel|Microsoft Invitation Acceptance Portal|Azure ESTS Service|Microsoft B2B Admin Worker|Microsoft Stream Portal|Microsoft Stream Service|Azure AD Cloud Sync|Azure AD PIM|Portfolios|ProjectWorkManagement|AAD Terms Of Use|({full_name}[\w,\s]+?))))\s+(\w+=|$)""",
    """"+UserId"+:"+((\w{1,5}:\w{1,5}:[^\#]+\#)?({email_address}[^@\s"]+?@({email_domain}[^@\s\."]+\.[^\s",]+))|({full_name}({first_name}[^"\s]+)\s({last_name}[^"]+))|(Unknown|({user_sid}[^"]+)))"+""",
    """"ClientIP":"(::1|\[?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\%\d+)?(:({src_port}\d+))?)"""",
    """\ssrc=\[?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s\w+=""",
    """"ResultStatus":"({result}[^"]+?)"""",
    """destinationServiceName\s*=({app}[^=]+?)\s+(\w+=|$)""",
    """\ssourceServiceName =(Core Directory|Account Provisioning|({app}[^=]+?))\s+(\w+=|$)""",
    """\WfilePath=(((?i)N\/A)|([A-Za-z\d]+)|({file_path}[^=]+?))\s*(\w+=|$)""",
    """\WfilePath=(((?i)N\/A)|(({file_dir}[^=]+?)\/({file_name}[^\/=]+?)))\s*(\w+=|$)""",
    """\WfilePath=[^=]*?(\.({file_ext}[^\/\.]*?))?\s*(\w+=|$)""",
    """"ClientProcessName":"({process_name}[^"]+)""",
    """"Workload":\s*"({app}[^"]+)""""
    """"UserType":"*({user_type}[^,}"]+)"*"""
  
}
```