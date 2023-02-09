#### Parser Content
```Java
{
Name = microsoft-m365auditlogs-kv-mailbox-item-create-create
  ParserVersion = v1.0.0
  Product = M365 Audit Logs
  Conditions = [ """SESSID=""", """RESULTCODE=""", """WORKLOAD=""", """COMMAND=Create """, """OBJECT=""" ]

logrhythm-o365-app-activity-1 = {
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """\sTS=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """USER=(Unknown|({email_address}[^@\s]+@[^\s\.]+?\.[^\s]+?)|({user}[^\s@]+)(@({domain}[^\s]+))?)\s+\w+=""",
    """WORKLOAD=({app}[^=]+?)\s+\w+=""",
    """RESULTCODE=({result}[^=]+?)\s+\w+=""",
    """ORIGINATINGSERVER=({src_host}[^\s]+)""",
    """COMMAND=({operation}[^=]+?)\s+\w+=""",
    """SIP=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """USERAGENT=\s*(|({user_agent}[^\n]+?))\s*(\w+=|$)""",
    """LOGONUSERSID=({user_sid}[^\s]+)""",
    """CLIENTPROCESSNAME=({process_name}[^=]+?)\s+\w+=""",
    """"Attachments\\*"+:[\s\\]*"+\s*({email_attachments}[^"\\]+)\s*""",
    """"Attachments\\*"+:[\s\\]*"+\s*({email_attachment}[^"\\;]+)\s*""",
    """InternetMessageId":"({message_id}[^"]+)"""",
    """"Subject":"\s*({email_subject}[^"}]+?)\s*""""
  
}
```