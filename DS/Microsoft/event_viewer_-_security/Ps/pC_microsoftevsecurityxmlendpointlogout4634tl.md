#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-logout-4634-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<eventid>4634</eventid>"
      "<timecreated systemtime="
      "<data name="
    ]
    Fields = [
      "(?i)<Message>({event_name}[^.。]+)"
      "(?i)({event_name}An account was logged off)"
      "(?i)<TimeCreated SystemTime=('|\")({time}\\d{4}-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)\\d+Z('|\")\\/>"
      "(?i)<Computer>([^<>]+?[\\\\\\/]+)?({host}[^<>]+)<\\/Computer>"
      "(?i)<EventID>({event_code}[^<]+)<\\/EventID>"
      "(?i)<Keywords>({result}[^<]+)</Keywords>"
      "(?i)<Data Name =('|\")LogonType('|\")>({login_type}\\d+)<\\/Data>"
      "(?i)<Data Name =('|\")TargetUserSid('|\")>({user_sid}[^<]+)<\\/Data>"
      "(?i)<Data Name =('|\")TargetDomainName('|\")>((?i)NT AUTHORITY|({domain}[^<]+))<\\/Data>"
      "(?i)<Data Name =('|\")TargetUserName('|\")>((?i)SYSTEM|({user}[^<]+))<\\/Data>"
      "(?i)<Data Name =('|\")TargetLogonId('|\")>({login_id}[^<]+)<\\/Data>"
    ]
  

}
```