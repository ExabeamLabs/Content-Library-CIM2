#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-activity-success-create
  Product = Microsoft 365
  ParserVersion = "v1.0.0"
  Conditions= [ """"MailboxOwnerUPN":"""", """"OriginatingServer":"""", """"Workload":"""", """"Operation":"Create"""", """"UserId":"""" ]
  Fields = ${MSO365ParsersTemplates.cef-microsoft-o365-app-activity.Fields}[
    """"MailboxOwnerUPN"+:"+({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""",
    """\ssuser=((\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|(Unknown|Microsoft Intune|Microsoft Teams (Templates )?Service(s)?|Microsoft Online Services|Office 365 (SharePoint|Exchange) Online|anonymous|EMPTY\.*|(\w{1,5}:\w{1,5}:[^\#]+\#)?({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\\s@]+)\\)?(system|Unknown|Signup|({user}[\w\.\-\!\#\^\~]{1,40}\$?))|(Sync Client|Office365 Backend Process|Device Registration Service|Managed Service Identity|Microsoft Substrate Management|Microsoft Approval Management|Office 365 Exchange Online|Office 365 SharePoint Online|Microsoft Office 365 Portal|Microsoft App Access Panel|Microsoft Invitation Acceptance Portal|Azure ESTS Service|Microsoft B2B Admin Worker|Microsoft Stream Portal|Microsoft Stream Service|Azure AD Cloud Sync|Azure AD PIM|Portfolios|ProjectWorkManagement|AAD Terms Of Use|({full_name}[\w,\s]+?))))\s+(\w+=|$)""",
    """"+UserId"+:"+((\w{1,5}:\w{1,5}:[^\#]+\#)?({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({full_name}({first_name}[^"\s]+)\s({last_name}[^"]+))|(Unknown|({user_sid}[^"]+)))"+""",
    """"ClientIP":"(::1|::ffff:|\[?(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)(\%\d+)?(\]:({src_port}\d+))?)"""",
    """\ssrc=\[?(::ffff:)?({src_ip}((\d{1,3}\.){3}\d{1,3}|[A-Fa-f\d]+:[a-fA-F\d:]+))\]?(:({src_port}\d+))?\s\w+=""",
    """suser=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|(({user_sid}S-[\w\-]+)|({user_id}(\w+\-){4}\w+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""",
    """"f3u\\*"*:\\*"*({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""
    """"OriginatingServer":(\s*|)"({host}\w+)\s*(\([^\)]+?\))?(\\r\\n)?"""",
    """"LogonType":({login_type}\d+)"""
    """CEF:([^\|"]*\|){5}({event_name}[^\|"]+)""",
    """"Operation":"({event_name}[^"]+?)\.?"""",
    """"op\\*"*:\\*"*({event_name}[^",\\\s]+)"""  
  ]

cef-microsoft-o365-app-activity = {
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """"CreationTime\\*"+:[\s\\]*"+({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
    """CEF:([^\|"]*\|){5}({operation}[^\|"]+)""",
    """\sflexString1=({event_name}[^=]+?)\.?\s+(\w+=|$)""",
    """"Operation":"({operation}[^"]+?)\.?"""",
    """\sfname=\s*(N\/A|({email_subject}[^=\s]+))""",
    """((fileType=(n\/a|N\/A|mail|calendar-event|note|message)[^\n]*?\sfname=\s*(N\/A|({email_subject}[^=]+?)))|(fileType=group[^\n]*?\sfname=\s*(N\/A|({group_name}[^=]+?)))|(fileType=(file|folder|attachment|report)[^\n]*?\sfname=\s*(N\/A|({file_name}[^=]+?)))|(fileType=process[^\n]*?\sfname=\s*(N\/A|({process_name}[^=]+?)))|(fileType=app(lication)?[^\n]*?\sfname=\s*(N\/A|({app}[^=]+?))))\s+(\w+=|$)""",
    """"Subject":"\s*({additional_info}[^"]+?)\s*"""",
    """\Wmsg=({additional_info}[^=]+?)\s+(\w+=|$)""",
    """"ResultStatus":"({result}[^"]+?)"""",
    """destinationServiceName\s*=({app}[^=]+?)\s+(\w+=|$)""",
    """sourceServiceName =(Core Directory|Account Provisioning|({app}[^=]+?))\s+(\w+=|$)""",
    """\WfilePath=(((?i)N\/A)|([A-Za-z\d]+)|({file_path}[^=]+?))\s*(\w+=|$)""",
    """\WfilePath=(((?i)N\/A)|(({file_dir}[^=]+?)\/({file_name}[^\/=]+?)))\s*(\w+=|$)""",
    """\WfilePath=[^=]*?(\.({file_ext}[^\/\.]*?))?\s*(\w+=|$)""",
    """"ClientProcessName":"({process_name}[^"]+)"""
    """"userAgent":"({user_agent}[^"]+)"""",
    """"os":"({os}[^"]+)"""",
    """"(browser|BrowserName)":"({browser}[^"]+)""""
    """"ClientInfoString":"({user_agent}[^"]+)",""",
    """"ActorInfoString":"({user_agent}[^"]+)","""
    """"Workload":\s*"({app}[^"]+)""""
    """"UserType":"*({user_type}[^,}"]+)"*"""
    """"op\\*"*:\\*"*({operation}[^",\\\s]+)"""
    """"wl\\*"*:\\*"*({app}[^",\\\s]+)"""
    """"von\\*"*:\\*"*({alert_subject}[^",\\]+)"""
  ] 

}
```