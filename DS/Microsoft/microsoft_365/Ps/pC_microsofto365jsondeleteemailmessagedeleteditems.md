#### Parser Content
```Java
{
Name = microsoft-o365-json-delete-email-message-deleteditems
  ParserVersion = v1.0.0
  ExtractionType = json
  Conditions = [""""Operation":""", """Delete""", """"Workload":"Exchange"""", """"AffectedItems":""" ]
  Fields = ${MSO365ParsersTemplates.m365-activity.Fields}[
    """"Subject\\*":[\s\\]*"({email_subject}.*?)"\}""",
    """"ParentFolder":\{"[^,]+?,"Path":"({src_email_folder}.+?)"\}"""
    """"OriginatingServer":"({host}\w+)\s*(\([^\)]+?\))?(\\r\\n)?"""",
    """\ssuser=((\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|(NOT-FOUND|Unknown|Sync|AirInvestigation|Sync Client|Office365 Backend Process|Device Registration Service|Microsoft Intune|Microsoft Teams Services|Microsoft Online Services|Office 365 SharePoint Online|anonymous|SecurityComplianceAlerts|SecurityComplianceInsights|(Microsoft\\[^@\s"]+)|EMPTY\.*|({email_address}[A-Za-z0-9!#$%&'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\\s@"]{1,50})\\)(system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))|({full_name}[\w,\s]+?)))\s{1,100}(\w+=|$)""",
    """"UserId":"((\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|(NOT-FOUND|Unknown|Sync|AirInvestigation|Sync Client|Office365 Backend Process|Device Registration Service|Microsoft Intune|Microsoft Teams Services|Microsoft Online Services|Office 365 SharePoint Online|anonymous|SecurityComplianceAlerts|SecurityComplianceInsights|(Microsoft\\[^@\s"]+)|EMPTY\.*|({email_address}[A-Za-z0-9!#$%&'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\\s@"]{1,50})\\)(system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))|({full_name}[\w,\s]+?)))"+""",
    """"ClientIP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"ClientIPAddress\\*":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"UserKey":"(anonymous|({user_id}[^@\"]+))""",
    """"LogonUserSid":"({user_sid}[^"]+)"""",
    """"Attachments\\*"+:[\s\\]*"+\s*({attachment}[^"\\]+?)\s*"""",
    """InternetMessageId":"({message_id}[^"]+)"""",
    """exa_json_path=$.OriginatingServer,exa_regex=({host}[\w\-\.]+)\s""",
    """exa_json_path=$.ClientIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.ClientIPAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.LogonUserSid,exa_field_name=user_sid""",
    """exa_json_path=$.UserKey,exa_regex=(anonymous|({user_id}[^@\"]+))""",
    """exa_json_path=$.AffectedItems[0].Attachments,exa_field_name=attachment""",
    """exa_json_path=$.AffectedItems[0].InternetMessageId,exa_field_name=message_id""",
    """exa_json_path=$.AffectedItems[0].Subject,exa_field_name=email_subject""",
    """exa_json_path=$.AffectedItems[0].ParentFolder.Path,exa_field_name=src_email_folder"""
  ]

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
    """"MailboxOwnerUPN":"({owner}[^"]+)""""
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
    """exa_json_path=$.MailboxOwnerUPN,exa_field_name=owner"""
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