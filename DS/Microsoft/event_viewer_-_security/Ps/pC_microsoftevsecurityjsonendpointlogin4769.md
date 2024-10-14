#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-4769"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "epoch_sec", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
  ExtractionType = json
  Conditions = [
    """4769"""
    """"TransmittedServices":""""
  ]
  Fields = [
    """({event_name}A Kerberos service ticket was requested)"""
    """"EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """"EventReceivedTime":\s*({time}\d+)"""
    """"timestamp":\s*({time}\d+)"""
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)\s[^\s]+\s"""
    """"+created"+:"+({time}[^"]+)"""
    """"TimeCreated"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\dZ)""""
    """"Computer"+:"+({host}[\w\-.]+)""""
    """"+(?:winlog\.)?computer_name"+:"+({host}[\w\-.]+)"""
    """"(?i)(Hostname|MachineName)":"({host}[\w\-.]*)"""
    """({event_code}4769)"""
    """"TargetUserName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    """"TargetDomainName":"({domain}[^."]+)"""
    """"ServiceName":"({src_host}[\w\-.]+\$)""""
    """"ServiceName":"({service_name}[^@"]+)""""
    """"TicketOptions":"({ticket_options}[^"]+)"""
    """"TicketEncryptionType":"({ticket_encryption_type}[^"]+)"""
    """"IpAddress":"(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """"Status":"({result_code}[^"]+)""",
    """Client Address(:|=)\s*(\\r|\\n|\\t)*(::[\w]+:)?(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))"""
    """Client Port:(\\n|\\r|\\t)*({src_port}\d+)"""
    """exa_json_path=$.Message,exa_regex=({event_name}A Kerberos service ticket was requested)""",
    """exa_json_path=$.message,exa_regex=({event_name}A Kerberos service ticket was requested)""",
    """exa_json_path=$.EventTime,exa_regex=time""",
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$..created,exa_field_name=time""",
    """exa_json_path=$..Computer,exa_regex=^({host}[\w\-.]+)$""",
    """exa_json_path=$..computer_name,exa_regex=^({host}[\w\-.]+)$""",
    """exa_json_path=$.MachineName,exa_regex=^({host}[\w\-.]+)$""",
    """exa_json_path=$.Hostname,exa_regex=^({host}[\w\-.]+)$""",
    """exa_regex=({event_code}4769)""",
    """exa_json_path=$..TargetUserName,exa_regex=^(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$""",
    """exa_json_path=$..TargetDomainName,exa_field_name=domain""",
    """exa_json_path=$..ServiceName,exa_regex=^({src_host}[\w\-.]+\$)$""",
    """exa_json_path=$..ServiceName,exa_field_name=service_name""",
    """exa_json_path=$..TicketOptions,exa_field_name=ticket_options""",
    """exa_json_path=$..TicketEncryptionType,exa_field_name=ticket_encryption_type""",
    """exa_json_path=$..IpAddress,exa_regex=^(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$""",
    """exa_json_path=$..Status,exa_field_name=result_code""",
    """exa_regex=Client Address(:|=)\s*(\\r|\\n|\\t)*(::[\w]+:)?(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))""",
    """exa_regex=Client Port:(\\n|\\r|\\t)*({src_port}\d+)"""
  ]
  DupFields = [
    "result_code->failure_code"
  ]


}
```