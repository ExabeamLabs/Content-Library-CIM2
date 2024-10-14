#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-4776-6"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = ["MMM dd HH:mm:ss yyyy", "yyyy-MM-dd'T'HH:mm:ss"]
  Conditions = [
    """attempted to validate the credentials for an account"""
    """Authentication Package"""
  ]
  Fields = [
    """({event_name}The (computer|domain controller) attempted to validate the credentials for an account)"""
    """({time}\d\d\d\d-\d\d-\d\d(\s|T)\d\d:\d\d:\d\d)"""
    """({host}[\w\-.]+)\s+({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+\s+(am|AM|pm|PM))"""
    """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
    """(?i)(((audit|success|failure)( |_)(success|audit|failure))|information)\s*(\s|\t|,|#\d+|<[^>]+>)\s*({host}[^=]+?)\s*(\s|\t|,|#\d+|<[^>]+>)\s*"""
    """({host}[\w.\-]+)\s*:\s+The computer attempted to validate the credentials for an account"""
    """({host}[^\s\/]+)\/Microsoft-Windows-Security-Auditing \(4776\)"""
    """(?i)(((audit|success|failure)( |_)(success|audit|failure))|information)\s*(\s|\t|,|#\d+|<[^>]+>)\s*(?!(?:[A-Fa-f:\d.]+))[^\t,#<\s.]+\.({domain}[^\s.",]+)"""
    """(?!(?:[A-Fa-f:\d.]+))[^\s\/.]+\.({domain}[^\s\/.]+)[^\s\/]*\/Microsoft-Windows-Security-Auditing \(4776\)"""
    """({event_code}4776)"""
    """The ({login_type_text}computer|domain)(\s\w+)? attempted to validate the credentials"""
    """Logon (?:a|A)ccount(:|=)\s*(({email_address}[^@\s]+?@[^\s]+?\.[^\s]+?)|((({full_name}[^:]+?\s[^\s]+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(?:(@|＠)({domain}[^\s.;,@=]+).*?)?))[\s;]*Source Workstation(:|=)([\s\\]+|(\s*\\*((({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)(:({src_port}\d+))?)|({src_host}[\w\-.]+?))[\s;]*))Error Code(:|=)"""
    """Logon (?:a|A)ccount(:|=)\s*(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^'\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)＠({domain}[^\s]+))"""
    """Error Code(:|=)\s*({result_code}[\w\-]+)"""
    """Source Workstation(:|=)([\s\\]+|(\s*\\*((({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)(:({src_port}\d+))?)|({src_host}.+?))[\s;]*))Error Code(:|=)"""
  ]
  ParserVersion = "v1.0.0"


}
```