#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-enable-success-4722-2"
Conditions = [
"""A user account was enabled"""
"""computer_name"""
"""event_id\":4722"""
]
ParserVersion = "v1.0.0"

cef-microsoft-o365-app-activity.Fields}[
    """"MailboxOwnerUPN"+:"+({email_address}([A-Za-z0-9]+[!#$%&'+\-\.\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""",
    """\ssuser=((\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|(Unknown|Microsoft Intune|Microsoft Teams (Templates )?Service(s)?|Microsoft Online Services|Office 365 (SharePoint|Exchange) Online|anonymous|EMPTY\.*|(\w{1,5}:\w{1,5}:[^\#]+\#)?({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\\s@]+)\\)?(system|Unknown|Signup|({user}[\w\.\-\!\#\^\~]{1,40}\$?))|(Sync Client|Office365 Backend Process|Device Registration Service|Managed Service Identity|Microsoft Substrate Management|Microsoft Approval Management|Office 365 Exchange Online|Office 365 SharePoint Online|Microsoft Office 365 Portal|Microsoft App Access Panel|Microsoft Invitation Acceptance Portal|Azure ESTS Service|Microsoft B2B Admin Worker|Microsoft Stream Portal|Microsoft Stream Service|Azure AD Cloud Sync|Azure AD PIM|Portfolios|ProjectWorkManagement|AAD Terms Of Use|({full_name}[\w,\s]+?))))\s+(\w+=|$)""",
    """"+UserId"+:"+((\w{1,5}:\w{1,5}:[^\#]+\#)?({email_address}([A-Za-z0-9]+[!#$%&'+\-\.\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({full_name}({first_name}[^"\s]+)\s({last_name}[^"]+))|(Unknown|({user_sid}[^"]+)))"+""",
    """"ClientIP":"(::1|::ffff:|\[?(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)(\%\d+)?(\]:({src_port}\d+))?)"""",
    """\ssrc=\[?(::ffff:)?({src_ip}((\d{1,3}\.){3}\d{1,3}|[A-Fa-f\d]+:[a-fA-F\d:]+))\]?(:({src_port}\d+))?\s\w+=""",
    """suser=(({email_address}([A-Za-z0-9]+[!#$%&'+\-\.\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|(({user_sid}S-[\w\-]+)|({user_id}(\w+\-){4}\w+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""",
    """"f3u\\*"*:\\*"*({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""
    """"OriginatingServer":(\s*|)"({host}\w+)\s*(\([^\)]+?\))?(\\r\\n)?"""",
    """"RecordType":\s*"*({object_type}[^,]+?)"*,""",
    """"LogonType":"({login_type}\d+)""",
    """"LogonUserSid":"({user_sid}[^"]+)"""",
    """"Attachments\\*"+:[\s\\]*"+\s*({attachment}[^"\\]+?)\s*""""
    """MailboxOwnerUPN":\s"({user_upn}[^"]+)",""",
    """"ParentFolder":[^=]+?"Path":"\\*({object}[^"]+)"""",
    """"Subject":"({email_subject}[^"]+?)\s*"""",
    """InternetMessageId":"({message_id}[^"]+)""""
  
}
```