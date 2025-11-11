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
      """"src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """"dst_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """"id":\d*({event_code}5137)""",
      """"firsttime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
      """"DomainID":"({domain}[^"]+)""",
      """"HostID":"({dest_host}({host}[^"]+))""",
      """"UserIDSrc":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
      """"Security_ID":"({user_sid}[^"]+)""",
      """"Source_Logon_ID":"({login_id}[^"]+)""",
      """"ObjectID":"({ds_object_dn}[^"]+)""",
      """"ObjectID":"[^"]*?({ds_object_ou}(OU|ou)[^"]+)""",
      """"Target_Class":"({object_type}[^"]+)""",
      """"Process_Name":"({process_name}[^"]+)""",
    ]
	ParserVersion = "v1.0.0"
  

}
```