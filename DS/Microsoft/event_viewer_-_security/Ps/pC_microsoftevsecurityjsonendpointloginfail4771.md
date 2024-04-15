#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-fail-4771"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """4771""", """Kerberos pre-authentication failed.""", """"TicketOptions""", """"ServiceName""", """"TargetUserName""" ]
  Fields = [
    """({event_name}Kerberos pre-authentication failed)"""
    """"created":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)"""",
    """"EventTime":\s*({time}\d+)"""
    """"EventTime":\s*"({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})""""
    """"TimeGenerated":"({time}[^"]*)"""
    """"TimeCreated"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """"Computer":"({host}[^"]+)""""
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)\s[^\s]+\s"""
    """@timestamp\\?"+:\\?"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
    """"(Hostname|MachineName|(?:winlog\.)?computer_name)\\?":\\?"({host}[^."\\]*)"""
    """({event_code}4771)"""
    """"(TargetSid|TargetDomainName)\\?":\\?"({user_sid}[^"\\]*)"""
    """"TargetUserName\\?":\\?"({user}[^"\\]*)"""
    """"ServiceName\\?":\\?"[^/]*\/({domain}[^"\\]*)""",
    """"Status_string":"({result_code}[^"]+)"""",
    """"(Status|TicketOptions)\\?":\\?"({result_code}[^"\\]*)"""
    """"((IpAddress)|(ip))\\?":\\?"(?:::[\w]+:)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\\?""""
  ]
  DupFields = [
    "host->dest_host"
    "result_code->failure_code"
  ]


}
```