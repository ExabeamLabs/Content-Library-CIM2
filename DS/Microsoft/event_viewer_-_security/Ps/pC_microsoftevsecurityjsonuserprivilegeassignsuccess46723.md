#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-user-privilege-assign-success-4672-3
    Vendor = Microsoft
    Product = Event Viewer - Security 
    ParserVersion = "v1.0.0"
	TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [ """McAfee_SIEM:""", """Special privileges assigned to new logon.""" ]
    Fields = [
      """({event_name}Special privileges assigned to new logon)""",
      """"src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """"dst_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """"id":\d*({event_code}4672)""",
      """"firsttime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
      """"DomainID":"({domain}[^"]+)""",
      """"HostID":"({host}[^"]+)""",
      """"UserIDSrc":"({user}[\w\.\-]{1,40}\$?)""",
      """"Security_ID":"({user_sid}[^"]+)""",
      """"Source_Logon_ID":"({login_id}[^"]+)""",
      """"Privileges":"({privileges}[^"]+)"""
      """({event_code}4672)"""
    ]
    DupFields = [ "host->dest_host" ]
  

}
```