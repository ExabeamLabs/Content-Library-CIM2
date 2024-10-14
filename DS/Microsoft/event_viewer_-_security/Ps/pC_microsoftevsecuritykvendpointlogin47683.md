#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-4768-3"
  ExtractionType = json
  Vendor = "Microsoft"  
  Product = "Event Viewer - Security" 
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd HH:mm:ss", "epoch_sec", "MMM dd HH:mm:ss yyyy","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "MM/dd/yyyy HH:mm:ss a"]
  Conditions = [  
    """A Kerberos authentication ticket (TGT) was requested"""  
    """Account Name"""  
    """Microsoft-Windows-Security-Auditing""" 
  ] 
  Fields = [  
    """(?i)({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (am|pm))"""
    """"TimeCreated"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""" 
    """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})""" 
    """TimeGenerated=({time}\d{10})"""
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """({event_name}A Kerberos authentication ticket \(TGT\) was requested)"""  
    """({host}[^\s\/]+)\/Microsoft-Windows-Security-Auditing \(4768\)"""  
    """(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(am|pm|\d{4}|({host}[\w\-.]+))\s*[a-zA-Z]+"""
    """({event_code}4768)"""  
    """Account Name(:|=)\s*(\\t|\\r|\\n)*({user}[\w\.\-\!\#\^\~]{1,40}\$?)(?:@.+?)?[\s;]*(\\t|\\r|\\n)*"?\s*Supplied Realm Name""" 
    """Client Address(:|=)\s*(\\t|\\r|\\n)*(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(\\t|\\r|\\n)*""" 
    """Result Code(:|=)\s*(\\t|\\r|\\n)*({result_code}\w+)[\s;]*(\\t|\\r|\\n)*.+?Ticket Encryption Type:"""  
    """Supplied Realm Name(:|=)\s*(\\t|\\r|\\n)*(-|({domain}[^\s]+?))[\s;]*(\\t|\\r|\\n)*User ID(:|=)""" 
    """Supplied Realm Name(:|=)\s*.*?User ID(:|=)\s*(\\t|\\r|\\n)*(?:NULL SID|({user_sid}S-[^\s]+?))[\s;]*(\\t|\\r|\\n)*Service Information"""  
    """Pre-Authentication Type:([\s;]*|(\\[nrt])*)({auth_type}\d+)"""
    """Computer(Name)?"*(=|:)"*({host}[\w\-\.]+)([^\s]*\s|;)?"*"""
    """"TicketOptions":"({ticket_options}[^"]+)"""
    """"TicketEncryptionType":"({ticket_encryption_type}[^"]+)"""
    """"ServiceName":"({service_name}[^"]+)"""
    """"Computer"+:"+({host}[\w\-.]+)""""
    """"IpAddress":"(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""

    """exa_json_path=$.TimeCreated,exa_field_name=time""",
    """exa_json_path=$.TimeGenerated,exa_field_name=time""",
    """exa_regex=({event_name}A Kerberos authentication ticket \(TGT\) was requested)"""
    """exa_regex=({event_code}4768)"""
    """exa_json_path=$.EventID,exa_field_name=event_code""",
    """exa_json_path=$.Message,exa_regex=Account Name(:|=)\s*(\\t|\\r|\\n)*({user}[\w\.\-\!\#\^\~]{1,40}\$?)(?:@.+?)?[\s;]*(\\t|\\r|\\n)*"?\s*Supplied Realm Name""",
    """exa_json_path=$.Message,exa_regex=Result Code(:|=)\s*(\\t|\\r|\\n)*({result_code}.+?)[\s;]*(\\t|\\r|\\n)*Ticket Encryption Type(:|=)""",
    """exa_json_path=$.Message,exa_regex=Client Address(:|=)\s*(\\t|\\r|\\n)*(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(\\t|\\r|\\n)*""",
    """exa_json_path=$.Message,exa_regex=Supplied Realm Name(:|=)\s*(\\t|\\r|\\n)*(-|({domain}[^\s]+?))[\s;]*(\\t|\\r|\\n)*User ID(:|=)""",
    """exa_json_path=$.Message,exa_regex=Supplied Realm Name(:|=)\s*.*?User ID(:|=)\s*(\\t|\\r|\\n)*(?:NULL SID|({user_sid}S-[^\s]+?))[\s;]*(\\t|\\r|\\n)*Service Information""",
    """exa_json_path=$.Message,exa_regex=Pre-Authentication Type:[\\t\s;]*({auth_type}[^\s]+)""",
    """exa_json_path=$.EventData.TicketOptions,exa_field_name=ticket_options""",
    """exa_json_path=$.EventData.TicketEncryptionType,exa_field_name=ticket_encryption_type""",
    """exa_json_path=$.EventData.ServiceName,exa_field_name=service_name""",
    """exa_json_path=$.Computer,exa_field_name=host""",
    """exa_json_path=$.EventData.IpAddress,exa_regex=(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  ] 
  DupFields = ["user->account"]
  ParserVersion = "v1.0.0"  
},  

{ 
  Name = microsoft-evsecurity-kv-endpoint-login-requested 
  ParserVersion = v1.0.0  
  Vendor = "Microsoft"  
  Product = "Event Viewer - Security" 
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"  
  Conditions = [ """A Kerberos authentication ticket (TGT) was requested""","""Account Name""", """Computer""" ]  
  Fields = [ 
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)\s({host}[\w\-\.]+)?""",
    """ComputerName =({host}[\w\-\.]+)""", 
    """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))""" 
    """({event_name}A Kerberos authentication ticket \(TGT\) was requested)"""  
    """({event_code}4768)"""  
    """Account Name(:|=)\s*(\\t)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(?:@.+?)?[\s;]*(\\r\s\\t)*?Supplied Realm Name""" 
    """Client Address(:|=)\s*(::[\w]+:)?(\\t)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""" 
    """Result Code(:|=)\s*(\\t)?({result_code}[^\s].+?)[\s;]*?(\\r\s\\t)*?Ticket Encryption Type(:|=)"""  
    """Supplied Realm Name(:|=)\s*(-|({domain}[^\s]+?))[\s;]*User ID(:|=)""" 
    """Supplied Realm Name(:|=)\s*.*?User ID(:|=)\s*(?:NULL SID|({user_sid}[^\s]+?))[\s;]*Service Information"""  
    """Pre-Authentication\sType(:|=)\s*(?:-|({auth_type}[^\s]+))"""
    """Supplied Realm Name:\s*(-|({domain}[^\s]+?))\s*(\\r\s\\t)?User"""
  ] 
DupFields = ["user->account", "result_code->failure_code"]
ParserVersion = "v1.0.0"  


}
```