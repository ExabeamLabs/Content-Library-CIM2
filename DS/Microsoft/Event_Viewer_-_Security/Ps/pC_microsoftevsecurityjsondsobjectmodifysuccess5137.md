#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-ds-object-modify-success-5137
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [ """McAfee_SIEM:""", """A directory service object was created.""" ]
    Fields = [
      """({event_name}A directory service object was created)""",
      """"src_ip":"({src_ip}[^"]+)""",
      """"dst_ip":"({dest_ip}[^"]+)""",
      """"id":\d*({event_code}5137)""",
      """"firsttime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
      """"DomainID":"({domain}[^"]+)""",
      """"HostID":"({host}[^"]+)""",
      """"UserIDSrc":"({user}[^"]+)""",
      """"Security_ID":"({user_sid}[^"]+)""",
      """"Source_Logon_ID":"({login_id}[^"]+)""",
      """"ObjectID":"({object_dn}[^"]+)""",
      """"ObjectID":"[^"]*?({object_ou}(OU|ou)[^"]+)""",
      """"Target_Class":"({object_class}[^"]+)""",
      """"Process_Name":"({process_name}[^"]+)""",
    ]
    DupFields = [ "host->dest_host" ]
	ParserVersion = "v1.0.0"
  

}
```