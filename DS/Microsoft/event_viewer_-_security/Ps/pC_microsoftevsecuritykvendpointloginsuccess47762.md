#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-success-4776-2"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [
    """attempted to validate the credentials for an account"""
    """Authentication Package"""
    """dhn"""
  ]
  Fields = [
    """({event_name}The (computer|domain controller) attempted to validate the credentials for an account)"""
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
    """(?i)(((audit|success|failure)( |_)(success|audit|failure))|information)\s*(\s|\t|,|#\d+|<[^>]+>)\s*(?!(?:[A-Fa-f:\d.]+))[^\t,#<\s.]+\.({domain}[^\s.",]+)"""
    """(?!(?:[A-Fa-f:\d.]+))[^\s\/.]+\.({domain}[^\s\/.]+)[^\s\/]*\/Microsoft-Windows-Security-Auditing \(4776\)"""
    """"dhn":"({host}[^-"]+)"""
    """"dhn":"(?!(?:[A-Fa-f:\d.]+))[^".]+\.({domain}[^-".]+)[^"-]*"""
    """<Computer>(?!(?:[A-Fa-f:\d.]+))[^<.]+\.({domain}[^.<]+)[^<]*</Computer>"""
    """Computer(Name)?\s*(:|=)\s*"?(?!(?:[A-Fa-f:\d.]+))[^\s."]+\.({domain}[^\s".]+)[^\s"]*("|\s)"""
    """({event_code}4776)"""
    """The ({login_type_text}computer|domain)(\s\w+)? attempted to validate the credentials"""
    """Logon (?:a|A)ccount(:|=)\s*(({email_address}[^@\s]+?@[^\s]+?\.[^\s]+?)|(({user}[^@\s,;=]+?)(?:@({domain}[^\s.;,@=]+).*?)?))[\s;]*Source Workstation(:|=)([\s\\]+|(\s*\\*((({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)(:({dest_port}\d+))?)|({dest_host}.+?))[\s;]*))Error Code(:|=)"""
    """Error Code(:|=)\s*({result_code}[\w\-]+)"""
    """Computer_name\s*:\s*({dest_host}[^\"\s]+)"""
    """Computer_name\s*:\s*({host}[^\"\s]+)"""
    """Source Workstation(:|=)([\s\\]+|(\s*\\*((({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)(:({src_port}\d+))?)|({src_host}.+?))[\s;]*))Error Code(:|=)"""
  ]
  ParserVersion = "v1.0.0"


}
```