#### Parser Content
```Java
{
Name = proofpoint-tappod-json-email-send-receive-rcpts
    ParserVersion = v1.0.0
    Vendor = Proofpoint
    Product = Proofpoint Email Protection
    ExtractionType = json
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ","yyyy-MM-dd'T'HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSSSS"]
    Conditions = [
""""subject"""",
""""from"""",
""""rcpts"""",
""""rule"""",
""":"""
    ]   
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)(\s+({host}[^:]+)\s)?""",   
      """("|')ts("|')+:\s*("|')+({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+[\+\-]\d+)""",
      """"from"+:\s*\[?"+?({full_name}[^"@\s,<>]+\s+[^"@,<>]+?)?\s*\<?(\\u\d+)?({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|\>]+)>*"],""",
      """"envelope":.+?"from":"({full_name}[^"@\s,<>]+\s+[^"@,<>]+?)?\s*\<?(\\u\d+)?({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|\>]+)>*"""",
      """"message-id":.+?"subject"+:\s*\["+({email_subject}[^"]+?\])""",
      """"msg":\{.+?"header".+?"subject":\["({email_subject}[^"]+?)"\]""",
      """"msg".+?"normalizedHeader":.+?"subject":\["({email_subject}[^"]+?)"\]"""
      """"rcpts"+:\s*\[({email_recipients}"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\]]*?)"\]""",
      """"verified"+:\{[^\}]*"rcpts"+:\s*\["({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\]]*?)"\]""",
      """"filter"+:.+?"+disposition"+:\s*"+({result}[^"]+)""",
      """"routeDirection"+:\s*"+({direction}[^"]+)""",
      """"message-id"+:\s*\["+<*({message_id}[^>"]+)""",
      """msgParts":[^\$]+"detectedName"+:\s*"+\s*({email_attachments}({email_attachment}[^",]+?\.({file_ext}\w+)))"""",
      """"detectedName":"({attachment_1}[^"]+)"(.+?detectedName":"({attachment_2}[^"]+)")?(.+?detectedName":"({attachment_3}[^"]+)")?(.+?detectedName":"({attachment_4}[^"]+)?")?(.+?detectedName":"({attachment_5}[^"]+)")?(.+?detectedName":"({attachment_6}[^"]+)")?(.+?detectedName":"({attachment_7}[^"]+)")?(.+?detectedName":"({attachment_8}[^"]+)")?(.+?detectedName":"({attachment_9}[^"]+)")?(.+?detectedName":"({attachment_10}[^"]+)")?"""
      """msgParts":[^\$]+"sizeDecodedBytes":\s*({bytes}\d+)""",
      """"sizeBytes"+:\s*({bytes}\d+)""",
      """"ip"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """"x-originating-ip"+:\s*\["+\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """"host"+:\s*"+\[?({host}[\w\-.]+)\]?"""",
      """"rules"+:\[[^\]]*"+rule"+:"+({rule}[^"]+)"""",
      """"guid"*:\s*"*({alert_id}[^"]+)"""",
      """"msgParts":\[\{[^\n]*"md5":"({hash_md5}[^"]+)"[^\n]*\],""",
      """"msgParts":\[\{[^\n]*"sha256":"({hash_sha256}[^"]+)"[^\n]*(\],|\}\])""",
      """"msg".+?normalizedHeader":.+?"reply-to":\["(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-]{1,40}\$?|({dest_user_full_name}\w+(\s+\w+)+)))"]""",
      """"msg".+?"normalizedHeader":.+?"from"+:\s*\[?"+?({full_name}[^"@\s,<>]+\s+[^"@,<>]+?)?\s*\<?(\\u\d+)?({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|\>]+)>?"?\]?,""""
      """"country":"({country}[^"]+)""",
      """"virusNames":\s*\["({virus_name}[^"]+)""",
      """"actions":\[.+?"action":"({action}[^"]+)"""",
      """"actions":\[.+?"rule":"({rule}[^"]+)"""",
      """\{[^\}]*?"rule":\s*"({rule}[^"]+)"[^\}]*?"isFinal":\s*true"""
      """\{[^\}]*?"action":\s*"({action}[^"]+)"[^\}]*?"isFinal":\s*true"""
      """\{[^\}]*?"isFinal":\s*true[^\}]*?"action":\s*"({action}[^"]+)""""
      """\{[^\}]*?"isFinal":\s*true[^\}]*?"rule":\s*"({rule}[^"]+)""""
      """"connection":.+?"resolveStatus":"({connection_status}[^"]+)"""",
      """"msg".+?"normalizedHeader":.+?"reply-to":\["[^",<>]+\s<({reply_to}[^>"]+)>"""",
      """msgParts":[^\n]*?"detectedName":"[^",]*(\.({file_ext}\w+))"""
      """"(classification|triggeredClassification|triggeredClassifier)":\s*"({alert_type}[^",]+)""",
      """exa_json_path=$.filter..triggeredClassifier,exa_field_name=alert_type""",
      """exa_json_path=$.filter..triggeredClassification,exa_field_name=alert_type""",
      """exa_json_path=$.filter..classification,exa_field_name=alert_type""",
      """exa_json_path=$.ts,exa_field_name=time""",
      """exa_regex="from"+:\s*\[?"+?({full_name}[^"@\s,<>]+\s+[^"@,<>]+?)?\s*\<?(\\u\d+)?({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|\>]+)>*"],""",
      """exa_json_path=$.envelope.from,exa_regex=({full_name}[^"@\s,<>]+\s+[^"@,<>]+?)?\s*\<?(\\u\d+)?({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|\>]+)>*($|")""",
      """exa_json_path=$.msg.normalizedHeader.subject[1:],exa_field_name=email_subject""",
      """exa_json_path=$.envelope.rcpts[1:],exa_regex=({email_recipients}"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\]]*?)""",
      """exa_json_path=$.filter.verified.rcpts[1:],exa_regex=({email_recipients}"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\]]*?)""",
      """exa_json_path=$.filter.disposition,exa_field_name=result""",
      """exa_json_path=$.filter.routeDirection,exa_field_name=direction""",
      """exa_json_path=$.connection.ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """exa_json_path=$.connection.host,exa_regex=\[?({host}[\w\-.]+)\]?""",
      """exa_regex="rules"+:\[[^\]]*"+rule"+:"+({rule}[^"]+)"""",
      """exa_json_path=$.guid,exa_field_name=alert_id""",
      """exa_json_path=$.connection.country,exa_field_name=country""",
      """exa_regex="actions":\[.+?"action":"({action}[^"]+)"""",
      """exa_regex="actions":\[.+?"rule":"({rule}[^"]+)"""",
      """exa_regex=\{[^\}]*?"rule":\s*"({rule}[^"]+)"[^\}]*?"isFinal":\s*true"""
      """exa_regex=\{[^\}]*?"action":\s*"({action}[^"]+)"[^\}]*?"isFinal":\s*true"""
      """exa_regex=\{[^\}]*?"isFinal":\s*true[^\}]*?"action":\s*"({action}[^"]+)""""
      """exa_regex=\{[^\}]*?"isFinal":\s*true[^\}]*?"rule":\s*"({rule}[^"]+)"""
      """exa_json_path=$.connection.resolveStatus,exa_field_name=connection_status""",
      """exa_regex="msg".+?"normalizedHeader":.+?"reply-to":\["[^",<>]+\s<({reply_to}[^>"]+)>""""
      """exa_regex="rcpts"+:\s*\["({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\]]*?)\]""",
      """exa_regex="verified"+:\{[^\}]*"rcpts"+:\s*\["({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\]]*?)"\]""",
      """exa_regex="message-id"+:\s*\["+<*({message_id}[^>"]+)""",
      """exa_regex=msgParts":[^\$]+"detectedName"+:\s*"+\s*({email_attachments}({email_attachment}[^",]+?\.({file_ext}\w+)))"""",
      """exa_regex="detectedName":"({attachment_1}[^"]+)"(.+?detectedName":"({attachment_2}[^"]+)")?(.+?detectedName":"({attachment_3}[^"]+)")?(.+?detectedName":"({attachment_4}[^"]+)?")?(.+?detectedName":"({attachment_5}[^"]+)")?(.+?detectedName":"({attachment_6}[^"]+)")?(.+?detectedName":"({attachment_7}[^"]+)")?(.+?detectedName":"({attachment_8}[^"]+)")?(.+?detectedName":"({attachment_9}[^"]+)")?(.+?detectedName":"({attachment_10}[^"]+)")?"""
      """exa_regex=msgParts":[^\$]+"sizeDecodedBytes":\s*({bytes}\d+)""",
      """exa_json_path=$.msg.sizeBytes,exa_field_name=bytes""",
	    """exa_regex="msgParts":\[\{[^\n]*"md5":"({hash_md5}[^"]+)"[^\n]*\],""",
      """exa_regex="msgParts":\[\{[^\n]*"sha256":"({hash_sha256}[^"]+)"[^\n]*(\],|\}\])""",
      """exa_regex="msg".+?"normalizedHeader":.+?"from"+:\s*\[?"+?({full_name}[^"@\s,<>]+\s+[^"@,<>]+?)?\s*\<?(\\u\d+)?({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|\>]+)>?"?\]?,""""
      """exa_regex="message-id":.+?"subject"+:\s*\["+({email_subject}[^"]+?\])""",
      """exa_regex="msg":\{.+?"header".+?"subject":\["({email_subject}[^"]+?)"\]""",
      """exa_regex="msg".+?"normalizedHeader":.+?"subject":\["({email_subject}[^"]+?)"\]"""
      """exa_regex=msgParts":[^\n]*?"detectedName":"[^",]*(\.({file_ext}\w+))"""
      """exa_json_path=$..normalizedHeader.subject[0:],exa_field_name=email_subject""",
    ]
  SOAR {
    IncidentType = "dlp"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "dest_email_address->dlpUser", "email_address->emailFrom", "email_subject->emailSubject", "email_recipients->emailTo", "action->dlpActionTaken","host->dlpDeviceName"]
    NameTemplate = """Proofpoint DLP email ${email_subject} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address"]

}
```