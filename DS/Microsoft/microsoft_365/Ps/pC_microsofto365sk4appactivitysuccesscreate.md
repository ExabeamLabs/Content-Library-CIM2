#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-activity-success-create
  Product = Microsoft 365
  ParserVersion = "v1.0.0"
  Conditions= [ """"MailboxOwnerUPN":"""", """"OriginatingServer":"""", """"Workload":"""", """"Operation":"Create"""", """"UserId":"""" ]
  Fields = ${MSO365ParsersTemplates.cef-microsoft-o365-app-activity.Fields}[
    """"MailboxOwnerUPN"+:"+({email_address}([A-Za-z0-9]+[!#$%&'+\-\.\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""",
    """\ssuser=((\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|(Unknown|Microsoft Intune|Microsoft Teams (Templates )?Service(s)?|Microsoft Online Services|Office 365 (SharePoint|Exchange) Online|anonymous|EMPTY\.*|(\w{1,5}:\w{1,5}:[^\#]+\#)?({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\\s@]+)\\)?(system|Unknown|Signup|({user}[\w\.\-\!\#\^\~]{1,40}\$?))|(Sync Client|Office365 Backend Process|Device Registration Service|Managed Service Identity|Microsoft Substrate Management|Microsoft Approval Management|Office 365 Exchange Online|Office 365 SharePoint Online|Microsoft Office 365 Portal|Microsoft App Access Panel|Microsoft Invitation Acceptance Portal|Azure ESTS Service|Microsoft B2B Admin Worker|Microsoft Stream Portal|Microsoft Stream Service|Azure AD Cloud Sync|Azure AD PIM|Portfolios|ProjectWorkManagement|AAD Terms Of Use|({full_name}[\w,\s]+?))))\s+(\w+=|$)""",
    """"+UserId"+:"+((\w{1,5}:\w{1,5}:[^\#]+\#)?({email_address}([A-Za-z0-9]+[!#$%&'+\-\.\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({full_name}({first_name}[^"\s]+)\s({last_name}[^"]+))|(Unknown|({user_sid}[^"]+)))"+""",
    """"ClientIP":"(::1|::ffff:|\[?(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)(\%\d+)?(\]:({src_port}\d+))?)"""",
    """\ssrc=\[?(::ffff:)?({src_ip}((\d{1,3}\.){3}\d{1,3}|[A-Fa-f\d]+:[a-fA-F\d:]+))\]?(:({src_port}\d+))?\s\w+=""",
    """suser=(({email_address}([A-Za-z0-9]+[!#$%&'+\-\.\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|(({user_sid}S-[\w\-]+)|({user_id}(\w+\-){4}\w+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""",
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
    """\WfilePath=((N\/A)|([A-Za-z\d]+)|({file_path}[^=]+?))\s*(\w+=|$)""",
    """\WfilePath=((N\/A)|(({file_dir}[^=]+?)\/({file_name}[^\/=]+?)))\s*(\w+=|$)""",
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
m365-activity = {
  Vendor = Microsoft
  Product = Microsoft 365
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """"CreationTime\\*"+:[\s\\]*"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"Operation\\*"+:[\s\\]*"+({operation}[^"\\\.]*)""",
    """\sfname=\s*({object}[^=]+?)\s*(\w+=|$)""",
    """"SourceFileName":"({object}[^"]+)""",
    """"ObjectId\\*"+:"?[\s\\]*"+(Unknown|Not Available|({object}[^"]+))",""",
    """"User-?Agent\\?".*?:\s*\\?"({user_agent}[^"\\]+?)\\?"""",
    """"Workload"*:\s*"*({app}[^"]+)"*""",
    """"ApplicationId":"?({app_id}[^"]+)"?,""",
    """"result":"({result}[^"]+)""",
    """"ResultStatus":"({result}[^"]+)"""",
    """\Wmsg=({additional_info}[^=]+)\s{1,100}(\w+=|$)""",
    """"AADSessionId":"({session_id}[^"]+)"""",
    """"SessionId":"({session_id}[^"]+)"""",
    """LogonType":({login_type}\d+)""",
    """"ClientProcessName":\s*"({process_name}[^"]+)""",
    """"ClientInfoString":\s*"({user_agent}[^"]+)","""
    """"ActorInfoString":\s*"({user_agent}[^"]+)","""
    """MailboxOwnerUPN":\s"(anonymous|({user_upn}[^"]+))",""",
    """"UserId":\s*"(anonymous|({user_upn}[^",]+))"""",
    """"InternalLogonType":({login_type}\d+)""",
    """"RecordType":\s*"*({object_type}[^,]+?)"*,""",
    """"UserType":"*({user_type}[^,}"]+)"*""",
    """\sfname=\s*(N\/A|({email_subject}[^=]+))\smsg=""",
    """((fileType=(n\/a|N\/A|mail|calendar-event|note|message)[^\n]*?\sfname=\s*(N\/A|({email_subject}[^=]+?)))|(fileType=group[^\n]*?\sfname=\s*(N\/A|({group_name}[^=]+?)))|(fileType=(file|folder|attachment|report)[^\n]*?\sfname=\s*(N\/A|({file_name}[^=]+?)))|(fileType=process[^\n]*?\sfname=\s*(N\/A|({process_name}[^=]+?)))|(fileType=app(lication)?[^\n]*?\sfname=\s*(N\/A|({app}[^=]+?))))\s+(\w+=|$)""",
    """"OrganizationId":"({tenant_id}[^"]+)","""
    """exa_json_path=$.CreationTime,exa_field_name=time"""
    """exa_json_path=$.Operation,exa_field_name=operation"""
    """exa_json_path=$.OrganizationId,exa_field_name=tenant_id"""
    """exa_json_path=$.RecordType,exa_field_name=object_type"""
    """exa_json_path=$.UserId,exa_regex=(anonymous|({user_upn}[^"]+))"""
    """exa_json_path=$.Workload,exa_field_name=app"""
    """exa_json_path=$.Workload,exa_field_name=resource"""
    """exa_json_path=$.ObjectId,exa_field_name=object_id"""
    """exa_json_path=$.ExtendedProperties,exa_field_name=more_info"""
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

}

}
#============================================== Start of WindowsParsers section ==================================================================
WindowsParsers = [
{
  Name = microsoft-evsecurity-cef-process-create-success-4688
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "epoch"
  Conditions = [
"""|Microsoft-Windows-Security-Auditing:4688|""",
"""|A new process has been created.|"""
  ]
  Fields = [
    """({event_name}A new process has been created)""",
    """\Wrt=({time}\d{13})""",
    """\Wdhost=({src_host}({host}[\w\-\.]+))\s*(\w+=|$)""",
    """\Wdvchost=({src_host}({host}[\w\-\.]+))\s*(\w+=|$)""",
    """\Wdst=({dest_ip}[a-fA-F:\.\d]+)\s*(\w+=|$)""",
    """({event_code}4688)""",
    """\Wduser=(?:-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*(\w+=|$)""",
    """\Wdntdom=(?:-|({domain}[^\s]+))\s*(\w+=|$)""",
    """\WdeviceNtDomain=(?:-|({domain}[^\s]+))\s*(\w+=|$)""",
    """\Wdproc=({process_path}({process_dir}(?:[^"]+?)?[\\\/])?({process_name}[^\\\/]+?))\s*(\w+=|$)""",
    """\Wdproc=({path}.+?)\s*(\w+=|$)""",
    """\Wduid=({login_id}[^\s]+)\s*(\w+=|$)""",
    """\Wcs2=({operation_type}.+?)\s*(\w+=|$)""",
    """\Wcs3=({process_id}({process_guid}[^\s]+))\s*(\w+=|$)""",
    """\Wcs4=({process_command_line}.+?)\s*(\w+=|$)""",
    """\Wcs4=\s*(|-|(sc|((?:[^"]+)?[\\\/])?sc.exe)\s*(?:\\*[\w.\-]+)?\s*create\s*({service_name}.+?))\s+binPath= ({process_path}({process_dir}(?:[^"]+?)?[\\\/])?({process_name}[^\\\/]+?))\s*(\w+=|$)""",
    """\Wcs5=({parent_process_guid}[^\s]+)\s*(\w+=|$)""",
    """\sfilePath=({parent_process_path}({parent_process_dir}(?:[^"]+?)?[\\\/])?({parent_process_name}[^\\\/]+?))\s*(\w+=|$)"""
  
}
```