#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-4768"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  ExtractionType = json
  Conditions = [
    """:4768"""
    """"ServiceName":""""
    """Pre-Authentication"""
  ]
  Fields = [
    """({event_name}A Kerberos authentication ticket \(TGT\) was requested)"""
    """"EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """"hostname":"({host}[\w\-\.]+)""""
    """"(Hostname|MachineName|(?:winlog\.)?computer_name)":"({host}[^"]*)"""
    """({event_code}4768)"""
    """"(TargetUserName|AccountName)":"\s*(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))"""
    """"(TargetDomainName|SuppliedRealmName)":"({domain}[^."]+)"""
    """"(UserID|TargetSid)":"({user_sid}[^"]+)"""
    """"(IpAddress|ClientAddress)":"(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """"(Status|ResultCode)":"({result_code}[^"]+)"""
    """"TicketOptions":"({ticket_options}[^"]+)"""
    """"TicketEncryptionType":"({ticket_encryption_type}[^"]+)"""
    """"ServiceName":"({service_name}[^"]+)""",
    """"PreAuthType":"({auth_type}[^"]+)"""",
    """Account Name:((\\)[rnt])*\s*({account}.+?)((\\)[rnt])*Supplied Realm"""
    """exa_json_path=$.EventTime,exa_field_name=time"""
    """exa_json_path=$.Hostname,exa_field_name=host"""
    """exa_json_path=$.EventID,exa_field_name=event_code"""
    """exa_json_path=$.TargetUserName,exa_regex=\s*(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))"""
    """exa_json_path=$.TargetDomainName,exa_field_name=domain"""
    """exa_json_path=$.TargetSid,exa_field_name=user_sid"""
    """exa_json_path=$.IpAddress,exa_regex=(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.Status,exa_field_name=result_code"""
    """exa_json_path=$.TicketOptions,exa_field_name=ticket_options"""
    """exa_json_path=$.TicketEncryptionType,exa_field_name=ticket_encryption_type"""
    """exa_json_path=$.ServiceName,exa_field_name=service_name"""
    """exa_json_path=$.PreAuthType,exa_field_name=auth_type"""
    """exa_regex=Account Name:((\\)[rnt])*\s*({account}.+?)((\\)[rnt])*Supplied Realm"""
    """exa_regex=({event_name}A Kerberos authentication ticket \(TGT\) was requested)"""
  ]


}
```