#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-4768"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
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
    """"(IpAddress|ClientAddress)":"(::[\w]+:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """"(Status|ResultCode)":"({result_code}[^"]+)"""
    """"TicketOptions":"({ticket_options}[^"]+)"""
    """"TicketEncryptionType":"({ticket_encryption_type}[^"]+)"""
    """"ServiceName":"({service_name}[^"]+)""",
    """"PreAuthType":"({auth_type}[^"]+)"""",
    """Account Name:((\\)[rnt])*\s*({account}.+?)((\\)[rnt])*Supplied Realm"""
  ]


}
```