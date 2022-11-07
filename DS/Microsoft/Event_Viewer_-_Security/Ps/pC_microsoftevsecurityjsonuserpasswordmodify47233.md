#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-user-password-modify-4723-3
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [ """McAfee_SIEM:""", """An attempt was made to change an account's password.""" ]
    Fields = [
      """({event_name}An attempt was made to change an account's password)""",
      """"src_ip":"({src_ip}[^"]+)""",
      """"dst_ip":"({dest_ip}[^"]+)""",
      """"id":\d*({event_code}4723)""",
      """"firsttime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
      """"DomainID":"({domain}[^"]+)""",
      """"HostID":"({host}[^"]+)""",
      """"UserIDSrc":"({user}[^"]+)""",
      """"Security_ID":"({user_sid}[^"]+)""",
      """"Source_Logon_ID":"({login_id}[^"]+)""",
      """"UserIDDst":"({dest_user}[^"]+)""",
      """"action":"({action}[^"]+)"""
    ]
    DupFields = [ "host->dest_host" ]
    ParserVersion = "v1.0.0"
  

}
```