#### Parser Content
```Java
{
Name = proofpoint-tap-cef-email-receive-fail-threatstatus
  ParserVersion = v1.0.0
  Conditions = [
"""CEF:""",
"""destinationServiceName =Proofpoint""",
""""threatStatus""""
  ]
  Fields = ${ProofpointParsersTemplates.s-proofpoint-email-in-1.Fields}[
    """"sha256"+:"+({hash_sha256}[^"]+)"+,"md5"+:"+({hash_md5}[^"]+)"+,\s*"filename":\s*"(?!text(\.txt|\.html|-calendar))""",
    """ Category \[({category}[^\]]+?)\]""",
    """"url":"\s*"([A-Fa-f\d]{64}|[^@]+@[^\.]+\.[^"]+|({malware_url}[^"]+))""",
    """"threat":\s*"([A-Fa-f\d]{64}|[^@]+@[^\.]+\.[^"]+|({malware_url}[^"]+))""",
    """threat":\s*"({malware_url}[^",]+?)\s*(,|")"""
    """"threat(Url|URL)":\s*"<?({threat_url}[^"]+?)"""",
    """(fromAddress|sender)":\s*\[?"({src_email_address}[^"\s,@]+@[^"\s,@]+\.[^"\s,@]+?)([\\]+)?([\\]+)?"\]?""",
    """toAddresses":\s*\[({email_recipients}"({dest_email_address}[^"\s@,;]+@[^"\s,;]+\.[^"\s,;]+)[^\]]*?)\]""",
    """"classification":\s*"({alert_name}[^"]+)""",
    """:\sCategory\s\[[^\]]+\]\s,\sName\s\[({alert_name}[^\]]+)\]""",
    """"fromArray":"({result}clicksBlocked|clicksPermitted|messagesBlocked|messagesDelivered)"""",
    """"threatStatus":"({status}[^"]+)""",
    """,\s*"filename":\s*"(?!text(\.txt|\.html|-calendar))\s*({email_attachments}({email_attachment}[^",;]+\.({file_ext}[^"]+))[^"]*?)",\s*"\w+":""",
    """"recipient":\["({dest_email_address}[^<]+)"],"""
  ]
  DupFields = ${ProofpointParsersTemplates.s-proofpoint-email-in-1.DupFields}[ "alert_type->alert_name","email_attachment->file_name","src_email_address->external_address","dest_email_address->email_address" ]

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
    """suser=({src_email_address}[^"\s,@]+@[^"\s,@]+)""",
    """duser=({dest_email_address}[^"\s,@]+@[^"\s,@]+)""",
    """sender":\s*"({src_email_address}[^"\s,@]+@[^"\s,@]+)""",
    """recipient":\s*\[?"({email_recipients}[^",;]+@[^",;]+[^"]*)""",
    """recipient":\s*\[?"({dest_email_address}[^",;]+@[^",;]+)""",
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
    """src-account-name":"({account_name}[^"]+)""",
    """"threatStatus":"({result}[^"]+)"""
  ]
  DupFields = [ "email_attachment->file_name" 
}
```