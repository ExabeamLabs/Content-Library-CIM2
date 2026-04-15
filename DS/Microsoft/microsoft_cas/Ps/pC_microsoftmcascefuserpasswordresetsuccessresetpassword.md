#### Parser Content
```Java
{
Name = "microsoft-mcas-cef-user-password-reset-success-resetpassword"
Conditions = [
"""CEF:"""
"""|MCAS|SIEM_Agent|"""
"""|Reset password|"""
]
ParserVersion = "v1.0.0"

account-password-activity-1.Fields}[
    """<Computer>({host}[^<]+)</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
	"""<EventID>({event_code}30009)</EventID>"""
  ]
 },
${MicrosoftParserTemplates.account-password-activity-1}{
  Name = microsoft-azuread-xml-user-password-reset-success-30029
  Vendor = Microsoft
  ParserVersion = "v1.0.0"
  Conditions = [ """<EventID>30029</EventID>""","""Microsoft-AzureADPasswordProtection-DCAgent""" ]
  Fields = ${MicrosoftParserTemplates.account-password-activity-1.Fields}[
    """<Computer>({host}[^<]+)</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
    """<EventID>({event_code}30029)</EventID>"""
  ]
 },

{
Vendor = "Microsoft"
Product = "Microsoft CAS"
TimeFormat = "epoch"
Fields = [
"""\|SIEM_Agent\|[^\|]*\|[^\|]*\|({operation}[^\|]+)\|"""
"""\|SIEM_Agent\|[^\|]*\|({event_name}[^\|]+)\|"""
"""\Wrt=({time}\d{13})"""
"""\Wdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
"""\WdestinationServiceName =({app}.+?)\s+(\w+=|$)"""
"""\Wsuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)"""
"""\Wsuser=({email_address}[^@\s]+@[^@\s]+)\s+(\w+=|$)"""
"""\Wc6a1=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
"""\Wmsg=({additional_info}.*?)\s+(\w+=|$)"""
]
Name = "microsoft-mcas-cef-user-password-reset-success-resetpassword"
Conditions = [
"""CEF:"""
"""|MCAS|SIEM_Agent|"""
"""|Reset password|"""
]
ParserVersion = "v1.0.0"
},

{
Name = "microsoft-evsecurity-kv-user-password-reset-success-4724-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
"""|McAfee|ESM"""
"""43-26304724"""
]
Fields = [
"""\|McAfee\|[^|]+?\|[^|]+?\|43-2630({event_code}\d+)(0|1)\|"""
"""({event_name}An attempt was made to reset an account's password)"""
"""\srt=({time}\d{13})"""
"""shost=({dest_host}({host}[\w\-.]+))"""
"""sntdom=({domain}[^\s]+)"""
"""dntdom=({dest_domain}[^\s]+)"""
"""suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
"""duser=({dest_user}.+?)\s+\w+="""
"""nitroSource_Logon_ID=({login_id}.+?)(\s|0\|)"""
"""nitroSecurity_ID=({user_sid}[^\s]+)"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"
},

{
Name = "microsoft-evsecurity-json-user-enable-success-auseraccountwasenabled"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""McAfee_SIEM:"""
"""A user account was enabled."""
]
Fields = [
"""({event_name}A user account was enabled)"""
""""src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""dst_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""""id":\d*({event_code}4722)"""
""""firsttime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""
""""DomainID":"({domain}[^"]+)"""
""""HostID":"({host}[^"]+)"""
""""UserIDSrc":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
""""Source_Logon_ID":"({login_id}[^"]+)"""
""""UserIDDst":"({dest_user}[^"]+)"""
]
ParserVersion = "v1.0.0"
},
{
Name = "microsoft-evsecurity-cef-user-enable-success-4722-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|McAfee|ESM"""
"""43-26304722"""
]
Fields = [
"""({event_name}A user account was enabled)"""
"""\|McAfee\|[^|]+?\|[^|]+?\|43-2630({event_code}\d+)(0|1)\|"""
"""\srt=({time}\d{13})(\s|0\||$)"""
"""\ssrc=({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?))(:({dest_port}\d+))?(\s|0\||$)"""
"""\sshost=({host}({dest_host}[\w\-.]+?))(\s|0\||$)"""
"""\ssntdom=({domain}[^\s]+?)(\s|0\||$)"""
"""\sdntdom=({dest_domain}[^\s]+?)(\s|0\||$)"""
"""\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+=|0\||\s*$)"""
"""\sduser=({dest_user}.+?)(\s+\w+=|0\||\s*$)"""
"""\snitroSource_Logon_ID=({login_id}.+?)(\s|0\||$)"""
]
ParserVersion = "v1.0.0"
},


{
Name = "microsoft-o365-json-email-send-fail-advancedhunting"
ExtractionType = json
Vendor = "Microsoft"
Product = "Microsoft Defender"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
Conditions = [
  """EmailAttachmentInfo""""
  """"NetworkMessageId":"""
  """"FileName":"""
  """"FileType":"""
]
Fields = [
  """"Timestamp":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""""
  """"RecipientEmailAddress":\s*"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
  """"SenderFromAddress":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)""""
  """"category":\s*"({category}[^"]+?)""""
  """"FileName":\s*"({email_attachment}({file_name}[^"\.]+?(\.({file_ext}[^"]+?)))?)""""
  """"FileType":\s*"({file_type}[^"]+?)""""
  """"NetworkMessageId":\s*"({message_id}[^"]+?)""""
  """"FileSize":({attachment_size}\d+)"""
  """"SHA256":\s*"({file_hash}[^",]+)"""
  """exa_json_path=$..Timestamp,exa_field_name=time"""
  """exa_json_path=$..time,exa_field_name=time"""
  """exa_json_path=$..RecipientEmailAddress,exa_regex=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """exa_json_path=$..SenderFromAddress,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
  """exa_json_path=$.category,exa_field_name=category"""
  """exa_json_path=$..FileName,exa_field_name=file_name"""
  """exa_json_path=$..FileName,exa_field_name=email_attachment"""
  """exa_json_path=$..FileType,exa_field_name=file_type"""
  """exa_json_path=$..NetworkMessageId,exa_field_name=message_id"""
  """exa_json_path=$..FileSize,exa_field_name=attachment_size"""
  """exa_json_path=$..SHA256,exa_field_name=file_hash"""
]
ParserVersion = "v1.0.0"
},

{
  Name = microsoft-o365-kv-app-login-fail-workload
  Vendor = Microsoft
  Product = Microsoft 365
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """SESSID=""", """RESULTCODE=""", """WORKLOAD=""", """COMMAND=UserLoginFailed""", """OBJECT=""" ]
  Fields = [
    """\sTS=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """USER=(Unknown|({email_address}[^@\s]+@[^\s\.]+?\.[^\s]+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^\s]+))?)\s+\w+=""",
    """DOMAIN=(|({domain}[^\s]+?))\s+\w+=""",
    """WORKLOAD=({app}[^=]+?)\s+\w+=""",
    """COMMAND=({event_name}[^=]+?)\s+\w+=""",
    """OBJECT=(Unknown|({object}[^=]+?))\s+\w+=""",
    """SIP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """RESULTCODE=({result}[^=]+?)\s+\w+=""",
    """USERAGENT=\s*(|({user_agent}[^\n]+?))\s*(\w+=|$)"""
  
}
```