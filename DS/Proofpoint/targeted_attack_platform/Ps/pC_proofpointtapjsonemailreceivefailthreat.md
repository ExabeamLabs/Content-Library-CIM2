#### Parser Content
```Java
{
Name = proofpoint-tap-json-email-receive-fail-threat
  log_timeFormat =  "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ParserVersion = v1.0.0
  Conditions = [
""""threatStatus":"""",
""""classification":"""",
""""threat":""",
"""messageID":""""
  ]
  Fields = ${ProofpointParsersTemplates.s-proofpoint-email-in-1.Fields}[
    """"sha256"+:"+({hash_sha256}[^"]+)"+,"md5"+:"+({hash_md5}[^"]+)"+,\s*"filename":\s*"(?!text(\.txt|\.html|-calendar))""",
    """ Category \[({category}[^\]]+?)\]""",
    """"url":"\s*"([A-Fa-f\d]{64}|[^@]+@[^\.]+\.[^"]+|({malware_url}[^"]+))""",
    """"threat":\s*"([A-Fa-f\d]{64}|[^@]+@[^\.]+\.[^"]+|({malware_url}[^"]+))""",
    """"threat(Url|URL)":\s*"<?({threat_url}[^"]+?)"""",
    """(fromAddress|sender)":\s*\[?"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))([\\]+)?([\\]+)?"\]?""",
    """toAddresses":\s*\[({email_recipients}"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\]]*?)\]""",
    """"classification":\s*"({alert_name}[^"]+)""",
    """:\sCategory\s\[[^\]]+\]\s,\sName\s\[({alert_name}[^\]]+)\]""",
    """"fromArray":"({result}clicksBlocked|clicksPermitted|messagesBlocked|messagesDelivered)"""",
    """"threatStatus":"({status_msg}[^"]+)""",
    """,\s*"filename":\s*"(?!text(\.txt|\.html|-calendar))\s*({email_attachments}({email_attachment}[^",;\/]+\.({file_ext}[^"]+))[^"]*?)",\s*"\w+":""",
    """"recipient":\["({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"],""",
    """proto=({alert_name}[^=]+)\s""",
    """msg=.*?\[({alert_source}[^\]]+)\]:""",
    """msg=.*?name:\s*({alert_source}[^\]]+)\]"""
    """"userAgent":"({user_agent}[^"]+)""""
    """"clickTime":"({log_time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""
    """"clickIP":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """"completelyRewritten":\s*({alert_status}(?i)true|false)"""
    """eventType=({result}[^\s]+)"""
  ]
  DupFields = ${ProofpointParsersTemplates.s-proofpoint-email-in-1.DupFields}[  "alert_name->alert_subject","email_attachment->file_name", "alert_name->alert_type" ]

s-proofpoint-email-in-1 = {
  Vendor = Proofpoint
  Product = Targeted Attack Platform
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
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
    """subject":\s*"\s*(\{\\|({email_subject}[^",]+?))\s*(,|")""",
    """suser=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|0-9]+))""",
    """duser=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """sender":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|0-9]+))""",
    """recipient":\s*\[?"({email_recipients}[^",;]+@[^",;]+[^"]*)""",
    """recipient":\s*\[?"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """GUID":\s*"({alert_id}[^",]+?)\s*(,|")""",
    """senderIP":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """url":\s*"([A-Fa-f\d]{64}|[^@,"]+@[^\.,"]+\.[^,"]+|({malware_url}[^",]+?))\s*(,|")""",
    """\scs1=Policy \[id: [^\]]*? ; name: ({alert_name}[^\]]+?) ; category: ({category}[^\]]+?)]""",
    """threat":\s*"\s*([A-Fa-f\d]{64}|[^@,]+@[^\.]+\.[^",]+|({malware_url}[^",]+?))\s*(,|")""",
    """,\s*"filename":\s*"(?!text(\.txt|\.html|-calendar))\s*({email_attachments}({email_attachment}[^",;]+)[^"]*?)",\s*"\w+":""",
    ""","fromArray":"({result}[^\]]+?)","\w+":""",
    """eventType":\s*"({result}[^",]+?)\s*(,|")""",
    """"messageID":\s*"<?({message_id}[^>"]+)""",
    """src-account-name":"({account_name}[^"]+)""",
    """"threatStatus":\s*"({result}[^"]+)""",
    """eventType=({result}[^\s]+)"""

    """exa_json_path=$.threatTime,exa_field_name=time""",
    """exa_json_path=$.messageTime,exa_field_name=time""",
    """exa_json_path=$.spamScore,exa_field_name=spam_score""",
    """exa_json_path=$.phishScore,exa_field_name=phishing_score""",
    """exa_json_path=$.malwareScore,exa_field_name=malware_score""",
    """exa_json_path=$.messageSize,exa_field_name=bytes""",
    """exa_json_path=$.classification,exa_field_name=alert_type""",
    """exa_json_path=$.threatsInfoMap[0].classification,exa_field_name=alert_type""",
    """exa_json_path=$.threatsInfoMap[0].threatType,exa_field_name=alert_type""",
    """exa_json_path=$.subject,exa_regex=(\{\\|({email_subject}[^",]+))""",
    """exa_json_path=$.sender,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|0-9]+))""",
    """exa_regex=recipient":\s*\[?"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_regex=recipient":\s*\[?"({email_recipients}[^",;]+@[^",;]+[^"]*)""",
    """exa_json_path=$.GUID,exa_field_name=alert_id""",
    """exa_json_path=$.senderIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_regex=url":\s*"({malware_url}[^",]+?)\s*(,|")""",
    """exa_regex=threat":\s*"\s*({malware_url}[^",]+?)\s*(,|")""",
    """exa_json_path=$.messageParts[0].filename,exa_regex=(?!text(\.txt|\.html|-calendar))\s*({email_attachments}({email_attachment}[^",;]+)[^"]*?)$""",
    """exa_json_path=$.fromArray,exa_field_name=result""",
    """exa_json_path=$.eventType,exa_field_name=result""",
    """exa_json_path=$.messageID,exa_regex=<?({message_id}[^>"]+)""",
    """exa_json_path=$.src-account-name,exa_field_name=account_name""",
    """exa_json_path=$.threatStatus,exa_field_name=result"""
    """exa_json_path=$.threatsInfoMap[0].threatUrl,exa_field_name=threat_url"""
    """exa_regex=({result}clicksBlocked|clicksPermitted|messagesBlocked|messagesDelivered)""",
    """exa_json_path=$.threatsInfoMap[0].threatUrl,exa_field_name=threat_url"""
    """exa_regex=eventType=({result}[^\s]+)"""
  ]
  DupFields = [ "email_attachment->file_name" 
}
```