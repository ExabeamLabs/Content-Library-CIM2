#### Parser Content
```Java
{
Name = proofpoint-tap-json-email-emailthreat
Conditions = [
"""Proofpoint"""
""""threatsInfoMap\":"""
""""threatTime\":"""
""""threat\":"""
""""threatUrl\":"""
]
ParserVersion = "v1.0.0"

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
    """suser=({sender}[^"\s,@]+@[^"\s,@]+)""",
    """duser=({dest_email_address}[^"\s,@]+@[^"\s,@]+)""",
    """sender":\s*"({sender}[^"\s,@]+@[^"\s,@]+)""",
    """recipient":\s*\[?"({email_recipients}[^",;]+@[^",;]+[^"]*)""",
    """recipient":\s*\[?"({dest_email_address}[^",;]+@[^",;]+)""",
    """GUID":\s*"({alert_id}[^",]+?)\s*(,|")""",
    """senderIP":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """url":\s*"([A-Fa-f\d]{64}|[^@,"]+@[^\.,"]+\.[^,"]+|({malware_url}[^",]+?))\s*(,|")""",
    """\scs1=Policy \[id: [^\]]*? ; name: ({alert_name}[^\]]+?) ; category: ({category}[^\]]+?)]""",
    """threat":\s*"\s*([A-Fa-f\d]{64}|[^@,]+@[^\.]+\.[^",]+|({malware_url}[^",]+?))\s*(,|")""",
    """,\s*"filename":\s*"(?!text(\.txt|\.html|-calendar))\s*({email_attachments}({email_attachment}[^",;]+)[^"]*?)",\s*"\w+":""",
    ""","fromArray":"({action}[^\]]+?)","\w+":""",
    """eventType":\s*"({action}[^",]+?)\s*(,|")""",
    """"messageID":\s*"<?({message_id}[^>"]+)""",
    """src-account-name":"({account_name}[^"]+)""",
    """src-account-name":"({account_name}[^"]+)""",
    """"threatStatus":"({result}[^"]+)"""
  ]
  DupFields = [ "email_attachment->file_name" 
}
```