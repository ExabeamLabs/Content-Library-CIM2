#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-4768-2"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
    """"EventID":"4768""""
    """A Kerberos authentication ticket (TGT) was requested"""
  ]
  Fields = [
    """({event_name}A Kerberos authentication ticket \(TGT\) was requested)"""
    """({event_code}4768)"""
    """"TimeCreated"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """"Computer"+:"+({host}[\w\-.]+)""""
    """"TicketOptions":"({ticket_options}[^"]+)"""
    """"TicketEncryptionType":"({ticket_encryption_type}[^"]+)"""
    """"ServiceName":"({service_name}[^"]+)"""
    """"Status":"({result_code}[^"]+)"""
    """"IpAddress":"(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """TargetUserName":"(?:-|(?i)(system|anonymous logon|LOCAL SERVICE|LOCAL SYSTEM)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""""
    """TargetDomainNam":"(?:-|({dest_domain}({domain}[^"]+?)))""""
    """TargetSid":"({dest_user_sid}({user_sid}[^"\\]+))""""
  ]


}
```