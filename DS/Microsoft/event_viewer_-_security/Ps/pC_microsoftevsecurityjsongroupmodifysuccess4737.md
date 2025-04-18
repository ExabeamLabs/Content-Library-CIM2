#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-group-modify-success-4737
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """A security-enabled global group was changed""", """"EventID":4737""",""""Channel":"Security"""" ]
  Fields = [
    """"EventTime":({time}\d{10})""",
    """"Hostname":"({host}[\w.-]+?)"""",
    """"EventID":({event_code}\d+)""",
    """({event_name}A security-enabled global group was changed)""",
    """"SubjectUserName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """"SubjectDomainName":"({domain}[^"]+)"""",
    """"SubjectUserSid":"({user_sid}[^"]+)""",
    """"SubjectLogonId":"({login_id}[^"]+)"""",
    """"Keywords":({result}[^,]+)"""
    """"TargetUserName":"({group_name}[^"]+)"""
    """"TargetDomainName":"({group_domain}[^"]+)""",
    """"TargetSid":"({group_id}[^"]+)""",
    """"PrivilegeList":"(-|({privileges}[^"]+))""",
# sam_account_name is removed
    """"SidHistory":"(-|({sid_history}[^"]+))""",
    """"ProcessID":({process_id}\d+)""",
    """"ThreadID":({thread_id}\d+)""",
   ]
   DupFields = ["user->src_user", "domain->src_domain"]


}
```