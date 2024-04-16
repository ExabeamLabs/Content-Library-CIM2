#### Parser Content
```Java
{
Name = "proofpoint-tap-json-email-receive-fail-proofpointtapmessagesblocked"
Vendor = "Proofpoint"
Product = "Targeted Attack Platform"
ExtractionType = json
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
 Conditions = [ """ProofPointTAPMessagesBlocked""", """sender_s":""", """"senderIP_s":""", """recipient_s":""" ]
Fields = [
"""exa_json_path=$.TimeGenerated,exa_field_name=time""",
"""exa_json_path=$.spamScore_d,exa_field_name=spam_score""",
"""exa_json_path=$.phishScore_d,exa_field_name=phishing_score""",
"""exa_json_path=$.malwareScore_d,exa_field_name=malware_score""",
"""exa_regex=classification\\*\"+:\s*\\*\"+({alert_type}[^\",]+?)\\*\s*\"""",
"""exa_json_path=$.subject_s,exa_field_name=email_subject""",
"""exa_regex="fromAddress_s\"+:\s*\"+\[(\\r|\\n)*\s*\\\"+({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\\""",
"""exa_regex="recipient_s\"+:\s*\"+\[(\\r|\\n)*\s*\\\"+({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\\""",
"""exa_json_path=$.GUID_s,exa_field_name=alert_id""",
"""exa_json_path=$.senderIP_s,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
"""exa_regex="filename\\*\"+:\s*\\*\"+({email_attachments}(?!text)[^\"\\]+)"""
"""exa_regex="md5\\*\"+:\s*\\*\"+({hash_md5}[^\\\"]+)"""
"""exa_regex="sha256\\*\"+:\s*\\*\"+({hash_sha256}[^\\\"]+)"""
"""exa_regex="threatStatus\\*\"+:\s*\\*\"+({status}[^\\\"]+)"""
"""exa_regex="threatID\\*\"+:\s*\\*\"+({threat_id}[^\\\"]+)"""
"""exa_regex="threatUrl\\*\"+:\s*\\*\"+({malware_url}[^\\\"]+)"""
"""exa_json_path=$.messageSize_d,exa_field_name=bytes""",
"""exa_regex="oContentType\\*\"+:\s*\\*\"+({mime}[^\\\"]+)"""
"""exa_json_path=$.QID_s,exa_field_name=query_id""",
"""exa_json_path=$.Type,exa_field_name=alert_name""",
"""exa_regex=({result}MessagesBlocked)"""
"""exa_json_path=$.SourceSystem,exa_field_name=log_source"""
]
DupFields = [
"dest_email_address->email_address"
]
ParserVersion = "v1.0.0"


}
```