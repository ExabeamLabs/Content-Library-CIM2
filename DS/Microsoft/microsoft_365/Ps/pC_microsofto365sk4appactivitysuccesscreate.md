#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-activity-success-create
  Product = Microsoft 365
  ParserVersion = "v1.0.0"
  Conditions= [ """destinationServiceName =Office 365""", """"Operation":"Create"""", """"UserId":"""" ]

cef-microsoft-o365-app-activity = {
  Vendor = Microsoft
  Product = Office 365
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """"CreationTime\\*"+:[\s\\]*"+({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
    """"OriginatingServer":"({dest_host}({host}\w+))\s*(\([^\)]+?\))?(\\r\\n)?"""",
    """CEF:([^\|"]*\|){5}({operation}[^\|"]+)""",
    """\sflexString1=({event_name}[^=]+?)\.?\s+(\w+=|$)""",
    """"Operation":"({operation}[^"]+?)\.?"""",
    """\sfname=\s*(N\/A|({log_subject}[^=\s]+))""",
    """((fileType=(n\/a|N\/A|mail|calendar-event|note|message)[^\n]*?\sfname=\s*(N\/A|({log_subject}[^=]+?)))|(fileType=group[^\n]*?\sfname=\s*(N\/A|({group_name}[^=]+?)))|(fileType=(file|folder|attachment|report)[^\n]*?\sfname=\s*(N\/A|({file_name}[^=]+?)))|(fileType=process[^\n]*?\sfname=\s*(N\/A|({process_name}[^=]+?)))|(fileType=app(lication)?[^\n]*?\sfname=\s*(N\/A|({app}[^=]+?))))\s+(\w+=|$)""",
    """\Wmsg=({additional_info}[^=]+?)\s+(\w+=|$)""",
    """\ssuser=((\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|(Unknown|Microsoft Intune|Microsoft Teams (Templates )?Service(s)?|Microsoft Online Services|Office 365 (SharePoint|Exchange) Online|anonymous|EMPTY\.*|(\w{1,5}:\w{1,5}:[^\#]+\#)?({email_address}[^@\s"]+@[^@\s\."]+\.[^\s",]+)|(({domain}[^\\\s@]+)\\)?(system|Unknown|Signup|({user}[^@\s]+))|(Sync Client|Office365 Backend Process|Device Registration Service|Managed Service Identity|Microsoft Substrate Management|Microsoft Approval Management|Office 365 Exchange Online|Office 365 SharePoint Online|Microsoft Office 365 Portal|Microsoft App Access Panel|Microsoft Invitation Acceptance Portal|Azure ESTS Service|Microsoft B2B Admin Worker|Microsoft Stream Portal|Microsoft Stream Service|Azure AD Cloud Sync|Azure AD PIM|Portfolios|ProjectWorkManagement|AAD Terms Of Use|({full_name}[\w,\s]+?))))\s+(\w+=|$)""",
    """"+UserId"+:"+((\w{1,5}:\w{1,5}:[^\#]+\#)?({email_address}[^@\s"]+?@({email_domain}[^@\s\."]+\.[^\s",]+))|({full_name}({first_name}[^"\s]+)\s({last_name}[^"]+))|(Unknown|({user_sid}[^"]+)))"+""",
    """"ClientIP":"(::1|::ffff:|\[?(::ffff:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)(\]:({src_port}\d+))?)"""",
    """\ssrc=\[?(::ffff:)?({src_ip}((\d{1,3}\.){3}\d{1,3}|[A-Fa-f\d]+:[a-fA-F\d:]+))\]?(:({src_port}\d+))?\s\w+=""",
    """"ResultStatus":"({result}[^"]+?)"""",
    """\sdestinationServiceName\s*=({app}[^=]+?)\s+(\w+=|$)""",
    """\ssourceServiceName =(Core Directory|Account Provisioning|({app}[^=]+?))\s+(\w+=|$)""",
    """\WfilePath=(((?i)N\/A)|([A-Za-z\d]+)|({file_path}[^=]+?))\s*(\w+=|$)""",
    """\WfilePath=(((?i)N\/A)|(({file_dir}[^=]+?)\/({file_name}[^\/=]+?)))\s*(\w+=|$)""",
    """\WfilePath=[^=]*?(\.({file_ext}[^\/\.]*?))?\s*(\w+=|$)""",
    """"ClientProcessName":"({process_name}[^"]+)"""
  
}
```