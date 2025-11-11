#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-fail-4771"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "dd/MM/yyyy hh:mm:ss a"]
  ExtractionType = json
  Conditions = [ """4771""", """Kerberos """, """"TicketOptions""", """"ServiceName""", """"TargetUserName""" ]
  Fields = [
    """({event_name}Kerberos pre-authentication failed)"""
    """"systemTime":"({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
    """"created":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)"""",
    """"EventTime\\*":\s*({time}\d+)"""
    """"EventTime\\*":\s*\\*"({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})\\*""""
    """"TimeGenerated":"({time}[^"]*)"""
    """"TimeCreated"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """"Computer":"({host}[\w\-.]+)""""
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)\s[^\s]+\s"""
    """@timestamp\\*"+:\\*"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
    """<TimeCreated SystemTime\\*=('|")?({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,9})?Z)"""
    """"(Hostname|MachineName|(?:winlog\.)?computer_name)\\*":\\*"({host}[\w\-\.]+)"""
    """({event_code}4771)"""
    """"(TargetSid|TargetDomainName)\\*":\\*"({dest_user_sid}({user_sid}[^"\\]*))"""
    """<Data Name ="TargetUserName">({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """"TargetUserName\\*":\\*"({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """"ServiceName\\*":\\*"[^/]*\/({domain}[^"\\]*)""",
    """"eventRecordID":"({event_id}\d+)""",
    """"severityValue":"({result}[^"]+?)\s*"""",
    """<Data Name\\*="Status">({failure_code}({result_code}[^<>]+))<\/Data>"""
    """"Status_string":"({failure_code}({result_code}[^"]+))"""",
    """"(Status|TicketOptions)\\*":\\*"({failure_code}({result_code}[^"\\]*))"""
    """"((IpAddress)|(ip))\\*":\\*"(?:::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\\*""""
    """exa_regex=({event_name}Kerberos pre-authentication failed)""",
    """exa_json_path=$..systemTime,exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """exa_json_path=$..EventTime,exa_field_name=time""",
    """exa_json_path=$..TimeGenerated,exa_field_name=time""",
    """exa_json_path=$..TimeCreated,exa_field_name=time""",
    """exa_json_path=$..@timestamp,exa_field_name=time""",
    """exa_json_path=$..computer,exa_regex=^({host}[\w\-.]+)$""",
    """exa_json_path=$..MachineName,exa_regex=^({host}[\w\-.]+)$""",
    """exa_json_path=$..Hostname,exa_regex=^({host}[\w\-.]+)$""",
    """exa_regex=({event_code}4771)""",
    """exa_json_path=$..TargetSid,exa_field_name=user_sid""",
    """exa_json_path=$..TargetDomainName,exa_field_name=user_sid""",
    """exa_json_path=$..TargetSid,exa_field_name=dest_user_sid""",
    """exa_json_path=$..TargetDomainName,exa_field_name=dest_user_sid""",
    """exa_json_path=$..TargetUserName,exa_regex=^({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))$""",
    """exa_json_path=$..ServiceName,exa_regex=^([\w\-.]+)\/({domain}[^\\\/\s"]+?)$""",
    """exa_json_path=$..eventRecordID,exa_field_name=event_id""",
    """exa_json_path=$..severityValue,exa_field_name=result""",
    """exa_json_path=$..Status,exa_field_name=result_code""",
    """exa_json_path=$..Status,exa_field_name=failure_code""",
    """exa_json_path=$..TicketOptions,exa_field_name=result_code""",
    """exa_json_path=$..TicketOptions,exa_field_name=failure_code""",
    """exa_json_path=$..IpAddress,exa_regex=^(?:::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$""",
    """exa_json_path=$..ip,exa_regex=^(?:::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$"""
  ]


}
```