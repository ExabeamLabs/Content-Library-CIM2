#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-ds-object-modify-success-4742
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """A computer account was changed.""" , """Service Principal Names:"""]
  Fields = [
    """"@timestamp"\s*:\s*"({time}.+?)"""",
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)\s[^\s]+\s""",
    """"(?:winlog\.)?computer_name"\s*:\s*"({host}[\w\-.]+?)"""",
    """({event_code}4742)""",
    """({event_name}A computer account was changed.)""",
    """SubjectDomainName"\s*:\s*"({domain}[^"]+)""",
    """SubjectUserName"\s*:\s*"({user}[\w\.\-]{1,40}\$?)"""
    """SubjectLogonId"\s*:\s*"({login_id}[^"]+)""",
    """TargetUserName"\s*:\s*"({dest_user}[^"]+)""",
    """ServicePrincipalNames"\s*:\s*"({attribute}[^"]+)"""
    """TargetDomainName"\s*:\s*"({object_dn}[^"]+)""",
    """TargetUserName"\s*:\s*"({src_host}[^\s$]+)\$"""
  ]
  DupFields = [ "host->dest_host"]


}
```