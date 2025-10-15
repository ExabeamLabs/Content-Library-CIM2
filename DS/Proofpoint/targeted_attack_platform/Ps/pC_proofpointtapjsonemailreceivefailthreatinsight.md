#### Parser Content
```Java
{
Name = proofpoint-tap-json-email-receive-fail-threatinsight
  ExtractionType = json
  log_timeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ParserVersion = v1.0.0  
  Conditions = [
"""threatinsight.proofpoint.com""",
"""sender":""",
""""senderIP":""",
"""recipient":"""
  ]
  Fields = ${ProofpointParsersTemplates.s-proofpoint-email-in-1.Fields}[
"""exa_json_path=$.threatID,exa_field_name=threat_id""",
"""exa_json_path=$.clickTime,exa_field_name=log_time""",
""""threatID":\s*"({threat_id}[^",]+?)\s*("|,)""",
""""clickTime":"({log_time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""
"""classification":\s*"({alert_name}[^",]+?)\s*(,|")""",
""""threatsInfoMap":\s*\[\{"[^}\]]+?"classification":\s*"({alert_name}[^"]+)""",
""""threatsInfoMap":\s*\[\{"[^}\]]+?"threatType":\s*"({alert_name}[^"]+)""",
"""exa_json_path=$.classification,exa_field_name=alert_name""",
"""exa_json_path=$.threatsInfoMap[0].classification,exa_field_name=alert_name""",
"""exa_json_path=$.threatsInfoMap[0].threatType,exa_field_name=alert_name"""
]

s-proofpoint-email-in-1 = {
  Vendor = Proofpoint
  Product = Targeted Attack Platform
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy-MM-dd'T'HH:mm:ssZ"]
  Fields = [
    """threatTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """messageTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """spamScore":\s*({spam_score}\d+)""",
    """phishScore":\s*({phishing_score}\d+)""",
    """(,|")malwareScore":\s*({malware_score}\d+)""",
    """messageSize":\s*({bytes}\d+)""",
    """classification":\s*"({alert_type}[^",]+?)\s*(,|")""",
    """"threatsInfoMap":\s*\[\{"[^}\]]+?"classification":\s*"({alert_type}[^"]+)""",
    """"threatsInfoMap":\s*\[\{"[^}\]]+?"threatType":\s*"({alert_type}[^"]+)""",
    """"subject":\s*"\s*(\{\\|({email_subject}.+?))\s*",\s*"(quarantineRule|quarantineFolder)""",
    """suser=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|0-9]+))""",
    """duser=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """sender":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|0-9]+))""",
    """recipient":\s*\[?"({email_recipients}[^",;]+@[^",;]+[^"]*)""",
    """recipient":\s*\[?"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """GUID":\s*"({alert_id}[^",]+?)\s*(,|")""",
    """senderIP":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """url":\s*"([A-Fa-f\d]{64}|[^@,"]+@[^\.,"]+\.[^,"]+|({malware_url}[^",]+?))\s*(,|")""",
    """\scs1=Policy \[id: [^\]]*? ; name: ({alert_name}[^\]]+?) ; category: ({category}[^\]]+?)]""",
    """threat":\s*"\s*([A-Fa-f\d]{64}|[^@,]+@[^\.]+\.[^",]+|({malware_url}[^",]+?))\s*(,|")""",
    """,\s*"filename":\s*"(?!text(\.txt|\.html|-calendar))\s*({email_attachments}({file_name}({email_attachment}[^",;]+))[^"]*?)",\s*"\w+":""",
    ""","fromArray":"({result}[^\]]+?)","\w+":""",
    """eventType":\s*"({result}[^",]+?)\s*(,|")""",
    """eventType=({result}[^\s]+)""",
    """"messageID":\s*"<?({message_id}[^>"]+)""",
    """src-account-name":"({account_name}[^"]+)""",
    """"threatStatus":\s*"({alert_status}[^"]+)""",
    """exa_json_path=$.threatTime,exa_field_name=time""",
    """exa_json_path=$.messageTime,exa_field_name=time""",
    """exa_json_path=$.spamScore,exa_field_name=spam_score""",
    """exa_json_path=$.phishScore,exa_field_name=phishing_score""",
    """exa_json_path=$.malwareScore,exa_field_name=malware_score""",
    """exa_json_path=$.messageSize,exa_field_name=bytes""",
    """exa_json_path=$.classification,exa_field_name=alert_type""",
    """exa_json_path=$.threatsInfoMap[0].classification,exa_field_name=alert_type""",
    """exa_json_path=$.threatsInfoMap[0].threatType,exa_field_name=alert_type""",
    """exa_json_path=$.subject,exa_field_name=email_subject""",
    """exa_json_path=$.sender,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|0-9]+))""",
    """exa_regex=recipient":\s*\[?"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_regex=recipient":\s*\[?"({email_recipients}[^",;]+@[^",;]+[^"]*)""",
    """exa_json_path=$.GUID,exa_field_name=alert_id""",
    """exa_json_path=$.senderIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_regex=url":\s*"({malware_url}[^",]+?)\s*(,|")""",
    """exa_regex=threat":\s*"\s*({malware_url}[^",]+?)\s*(,|")""",
    """exa_json_path=$.messageParts[0].filename,exa_regex=(?!text(\.txt|\.html|-calendar))\s*({email_attachments}({file_name}({email_attachment}[^",;]+))[^"]*?)$""",
    """exa_json_path=$.fromArray,exa_field_name=result""",
    """exa_json_path=$.eventType,exa_field_name=result""",
    """exa_regex=({result}clicksBlocked|clicksPermitted|messagesBlocked|messagesDelivered)""",
    """exa_regex=eventType=({result}[^\s]+)"""
    """exa_json_path=$.messageID,exa_regex=<?({message_id}[^>"]+)""",
    """exa_json_path=$.src-account-name,exa_field_name=account_name""",
    """exa_json_path=$.threatStatus,exa_field_name=alert_status"""
    """exa_json_path=$.threatsInfoMap[0].threatUrl,exa_field_name=threat_url"""
    """eventTime=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""
  
}
```