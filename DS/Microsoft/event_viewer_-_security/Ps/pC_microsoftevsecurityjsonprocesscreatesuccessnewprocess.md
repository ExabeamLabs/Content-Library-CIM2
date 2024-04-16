#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-process-create-success-newprocess
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [ """McAfee_SIEM:""", """A new process has been created""" ]
    Fields = [
      """({event_name}A new process has been created)""",
      """"src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """"dst_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """"id":\d*({event_code}4688)""",
      """"firsttime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
      """"DomainID":"({domain}[^"]+)""",
      """"HostID":"({host}({src_host}[\w\-.]+))""",
      """"UserIDSrc":"({user}[\w\.\-]{1,40}\$?)""",
      """"Security_ID":"({user_sid}[^"]+)""",
      """"Process_Name":"({process_path}({process_dir}[^"]*?)(\\u005|[\\\/])*({process_name}[^\\\/"]+?))"""",
      """"Source_Logon_ID":"({login_id}[^"]+)"""
    ]
        ParserVersion = "v1.0.0"
  

}
```