#### Parser Content
```Java
{
Name = microsoft-m365auditlogs-kv-email-send-success-sendonbehalf
  ParserVersion = v1.0.0
  Conditions = [ """SESSID=""", """RESULTCODE=""", """WORKLOAD=""", """COMMAND=SendOnBehalf""", """ORGANIZATIONNAME=""", """OBJECT=""" ]
  Fields = ${DLMicrosoftParsersTemplates.logrhythm-o365-app-activity-1.Fields}[
    """SENDONBEHALFOFUSER=({target}[^=]+?)(\s|$)"""
  ]

logrhythm-o365-app-activity-1 = {
  Vendor = LogRhythm
  Product = LogRhythm
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """\sTS=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """USER=(Unknown|({email_address}[^@\s]+@[^\s\.]+?\.[^\s]+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^\s]+))?)\s+\w+=""",
    """WORKLOAD=({app}[^=]+?)\s+\w+=""",
    """RESULTCODE=({result}[^=]+?)\s+\w+=""",
    """ORIGINATINGSERVER=({host}[^\s]+)""",
    """COMMAND=({operation}[^=]+?)\s+\w+=""",
    """SIP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """USERAGENT=\s*(|({user_agent}[^\n]+?))\s*(\w+=|$)""",
    """LOGONUSERSID=({user_sid}[^\s]+)""",
    """CLIENTPROCESSNAME=({process_name}[^=]+?)\s+\w+=""",
    """"Attachments\\*"+:[\s\\]*"+\s*({email_attachments}[^"\\]+)\s*""",
    """"Attachments\\*"+:[\s\\]*"+\s*({email_attachment}[^"\\;]+)\s*""",
    """InternetMessageId":"({message_id}[^"]+)"""",
    """"Subject":"\s*({email_subject}[^"}]+?)\s*""""
    """"Attachments\\*"+:[\s\\]*"+\s*[^"\\;]*(\.({file_ext}\w+))"""
  
}
```