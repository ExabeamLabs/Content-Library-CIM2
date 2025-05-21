#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-success-4776-2"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = [
    """attempted to validate the credentials for an account"""
    """Authentication Package"""
    """dhn"""
  ]
  Fields = [
    """({event_name}The (computer|domain controller) attempted to validate the credentials for an account)"""
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
    """({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(?i)(AM|PM))"""
    """(?i)(((audit|success|failure)( |_)(success|audit|failure))|information)\s*(\s|\t|,|#\d+|<[^>]+>)\s*(?!(?:[A-Fa-f:\d.]+))[^\t,#<\s.]+\.({domain}[^\s.",]+)"""
    """(?!(?:[A-Fa-f:\d.]+))[^\s\/.]+\.({domain}[^\s\/.]+)[^\s\/]*\/Microsoft-Windows-Security-Auditing \(4776\)"""
    """"dhn":"({host}[^-"]+)"""
    """"dhn":"(?!(?:[A-Fa-f:\d.]+))[^".]+\.({domain}[^-".]+)[^"-]*"""
    """<Computer>(?!(?:[A-Fa-f:\d.]+))[^<.]+\.({domain}[^.<]+)[^<]*</Computer>"""
    """Computer(Name)?\s*(:|=)\s*"?(?!(?:[A-Fa-f:\d.]+))[^\s."]+\.({domain}[^\s".]+)[^\s"]*("|\s)"""
    """({event_code}4776)"""
    """The ({login_type_text}computer|domain)(\s\w+)? attempted to validate the credentials"""
    """Logon (?:a|A)ccount(:|=)\s*(({user_upn}[^@\s]+?@[^\s]+?\.[^\s]+?)|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(?:@({domain}[^\s.;,@=]+).*?)?))[\s;]*Source Workstation(:|=)([\s\\]+|(\s*\\*((({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)(:({src_port}\d+))?)|({src_host}[\w\-.]+?))[\s;]*))Error Code(:|=)"""
    """Error Code(:|=)\s*({result_code}[\w\-]+)"""
    """Computer_name\s*:\s*({host}[\w\-.]+)"""
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
    """Source Workstation(:|=)([\s\\]+|(\s*\\*((({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)(:({src_port}\d+))?)|({src_host}[\w\-\.]+))[\s;]*))\w+\s*\w+(:|=)"""
    """Logon Account:\s*((?-i)\\+[rnt])*({account}[^\s].+?)\s*(\\r\s)?Source Workstation:"""
    """Source Workstation:\s*({src_host}[^\s]+?)\s(\\r\s)?Error Code:"""
    """Computer(Name)?\s*(:|=)\s*[^.\s]+(\.({domain}[^\s]+))?"""
  ]
  ParserVersion = "v1.0.0"


}
```