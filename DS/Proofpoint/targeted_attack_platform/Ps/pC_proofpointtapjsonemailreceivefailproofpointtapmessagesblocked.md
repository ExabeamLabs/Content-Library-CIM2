#### Parser Content
```Java
{
Name = "proofpoint-tap-json-email-receive-fail-proofpointtapmessagesblocked"
Vendor = "Proofpoint"
Product = "Targeted Attack Platform"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
 Conditions = [ """ProofPointTAPMessagesBlocked""", """sender_s":""", """"senderIP_s":""", """recipient_s":""" ]
Fields = [
"""threatTime\\*\"+:\s*\\*\"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""
"""spamScore_d\"+:\s*\"+({spam_score}\d+)"""
"""phishScore_d\"+:\s*\"+({phishing_score}\d+)"""
""""malwareScore_d\"+:\s*\"+({malware_score}\d+)"""
"""classification\\*\"+:\s*\\*\"+({alert_type}[^\",]+?)\\*\s*\""""
""""subject_s\"+:\s*\"+({email_subject}[^\",]+?)\s*\""""
""""fromAddress_s\"+:\s*\"+\[(\\r|\\n)*\s*\\\"+({src_email_address}[^\",;]+@[^\",;]+[^\"]*)\\"""
""""recipient_s\"+:\s*\"+\[(\\r|\\n)*\s*\\\"+({dest_email_address}[^\",;]+@[^\",;]+[^\"]*)\\"""
"""GUID_s\"+:\s*\"+({alert_id}[^\",]+?)\s*\""""
"""senderIP_s\"+:\s*\"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""filename\\*\"+:\s*\\*\"+({email_attachments}(?!text)[^\"\\]+)"""
""""md5\\*\"+:\s*\\*\"+({hash_md5}[^\\\"]+)"""
""""sha256\\*\"+:\s*\\*\"+({hash_sha256}[^\\\"]+)"""
""""threatStatus\\*\"+:\s*\\*\"+({status}[^\\\"]+)"""
""""threatID\\*\"+:\s*\\*\"+({threat_id}[^\\\"]+)"""
""""threatUrl\\*\"+:\s*\\*\"+({malware_url}[^\\\"]+)"""
""""messageSize_d\\*\"+:\s*\\*\"+({bytes}\d+)"""
""""oContentType\\*\"+:\s*\\*\"+({mime}[^\\\"]+)"""
""""QID_s\\*\"+:\s*\\*\"+({query_id}[^\\\"]+)"""
""""Type\\*\"+:\s*\\*\"+({alert_name}[^\\\"]+)"""
"""({result}MessagesBlocked)"""
""""SourceSystem\"+:\"+({log_source}[^\"]+)"""
]
DupFields = [
"dest_email_address->email_address"
]
ParserVersion = "v1.0.0"


}
```