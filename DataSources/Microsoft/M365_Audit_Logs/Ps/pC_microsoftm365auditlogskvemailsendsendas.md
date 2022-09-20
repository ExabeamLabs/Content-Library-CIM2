#### Parser Content
```Java
{
Name = microsoft-m365auditlogs-kv-email-send-sendas
  ParserVersion = v1.0.0
  Product = M365 Audit Logs
  Conditions = [ """SESSID=""", """RESULTCODE=""", """WORKLOAD=""", """COMMAND=SendAs""", """ORGANIZATIONNAME=""", """OBJECT=""" ]
  Fields = ${DLMicrosoftParsersTemplates.logrhythm-o365-app-activity-1.Fields}[
    """SENDASUSER=({target}[^\s]+)"""
  ]

logrhythm-o365-app-activity-1 = {
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """\sTS=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """USER=(Unknown|({email_address}[^@\s]+@[^\s\.]+?\.[^\s]+?)|({user}[^\s@]+)(@({email_domain}[^\s]+))?)\s+\w+=""",
    """WORKLOAD=({app}[^=]+?)\s+\w+=""",
    """RESULTCODE=({result}[^=]+?)\s+\w+=""",
    """ORIGINATINGSERVER=({src_host}[^\s]+)""",
    """COMMAND=({operation}[^=]+?)\s+\w+=""",
    """SIP=({src_ip}[a-fA-F\d:.]+)""",
    """USERAGENT=\s*(|({user_agent}[^\n]+?))\s*(\w+=|$)""",
    """LOGONUSERSID=({user_sid}[^\s]+)""",
    """CLIENTPROCESSNAME=({process_name}[^=]+?)\s+\w+=""",
    """"Attachments\\*"+:[\s\\]*"+\s*({email_attachments}[^"\\]+)\s*""",
    """"Attachments\\*"+:[\s\\]*"+\s*({email_attachment}[^"\\;]+)\s*""",
    """InternetMessageId":"({message_id}[^"]+)"""",
    """"Subject":"\s*({email_subject}[^"}]+?)\s*""""
  
}
```