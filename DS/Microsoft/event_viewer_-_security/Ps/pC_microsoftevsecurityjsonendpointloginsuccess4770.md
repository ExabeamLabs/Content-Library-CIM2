#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-success-4770"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd HH:mm:ss", "epoch_sec"]
  ExtractionType = json
  Conditions = [
    """4770"""
    """"A Kerberos service ticket was renewed."""
    """"TicketEncryptionType"""
  ]
  Fields = [
    """({event_name}A Kerberos service ticket was renewed)"""
    """"EventTime":\s*({time}\d+)"""
    """"timestamp\\*":\s*({time}\d+)"""
    """"+created"+:"+({time}[^"]+)"""
    """"EventTime":\s*"({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})""""
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)\s[^\s]+\s"""
    """@timestamp\\?"+:\\?"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
    """"(MachineName|Hostname|(?:winlog\.)?computer_name)\\?":\\?"({host}[\w\-.]+)"""
    """({event_code}4770)"""
    """"TargetDomainName\\?":\\?"({domain}[^."\\]*)"""
    """"TargetUserName\\?":\\?"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    """"ServiceName":"(({service_name}[^_"]+?)(_[^"\<]+?)?)"""",
    """"ServiceName\\?":\\?"({dest_host}[\w\-.]*\$)"""
    """"TicketOptions\\?":\\?"({ticket_options}[^"\\]*)"""
    """"TicketEncryptionType\\?":\\?"({ticket_encryption_type}[^"\\]*)"""
    """"IpAddress\\?":\\?"(?:::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\\?""""
    """Account Name:((?-i)\\+[rnt])*({account}.+?)((?-i)\\+[rnt])*Account Domain"""
    """exa_regex=({event_name}A Kerberos service ticket was renewed)""",
    """exa_json_path=$.EventTime,exa_field_name=time""",
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$..created,exa_field_name=time""",
    """exa_json_path=$.@timestamp,exa_field_name=time""",
    """exa_json_path=$.MachineName,exa_regex=^({host}[\w\-.]+)$""",
    """exa_json_path=$.Hostname,exa_regex=^({host}[\w\-.]+)$""",
    """exa_json_path=$..computer_name,exa_regex=^({host}[\w\-.]+)$""",
    """exa_regex=({event_code}4770)""",
    """exa_json_path=$..TargetDomainName,exa_field_name=domain""",
    """exa_json_path=$..TargetUserName,exa_regex=^(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$""",
    """exa_json_path=$..ServiceName,exa_field_name=service_name""",
    """exa_json_path=$..ServiceName,exa_regex=^({dest_host}[\w\-.]*\$)$""",
    """exa_json_path=$..TicketOptions,exa_field_name=ticket_options""",
    """exa_json_path=$..TicketEncryptionType,exa_field_name=ticket_encryption_type""",
    """exa_json_path=$..IpAddress,exa_regex=^(?:::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\\?$""",
    """exa_regex=Account Name:((?-i)\\+[rnt])*({account}.+?)((?-i)\\+[rnt])*Account Domain"""
  ]


}
```