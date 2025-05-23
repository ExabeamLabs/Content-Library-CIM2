#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-handle-request-success-4656
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ """"EventId":"4656"""", """A handle to an object was requested""" ]
  Fields = [
    """({event_name}A handle to an object was requested)""",
    """({operation_type}requested)""",
    """"TimeCreated":"({time}\d{13})"""",
    """"EventId":"({event_code}[^"]+)"""",
    """"Computer":"({host}[^"]+)"""",
    """"EventRecordID":"({event_id}[^"]+)"""",
    """"ThreadID":"({thread_id}[^"]+)"""",
    """"SubjectUserSid":"({user_sid}[^"]+)"""",
    """"SubjectUserName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """"SubjectDomainName":"({domain}[^"]+)"""",
    """"SubjectLogonId":"({login_id}[^"]+)"""",
    """"HandleId":"({handle_id}[^"]+)"""",
    """"TransactionId":"({transaction_id}[^"]+)"""",
    """"AccessList":"({access}[^"]+)"""",
    """"ProcessID":"({process_id}[^"]+)"""",
    """"ProcessName":"({process_path}[^"]+)"""",
    """"ObjectType":"({object_type}[^"]+)"""",
    """"ObjectName":"({object}[^"]+)"""",
    """"ObjectServer":"({object_server}[^"]+)"""",
    """"HandleId":"({object_id}[^"]+)"""",
  ]
  DupFields = [ "host->dest_host", "access->privileges", "user->src_user", "domain->src_domain" ]


}
```