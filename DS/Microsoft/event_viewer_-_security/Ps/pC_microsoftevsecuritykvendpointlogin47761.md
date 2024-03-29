#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-login-4776-1
  ParserVersion = v1.0.0
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = ["""attempted to validate the credentials for an account""", """Authentication Package""", """computer_name"""]
    Fields = [
      """({event_name}The (computer|domain controller) attempted to validate the credentials for an account)""",
      """(?i)(((audit|success|failure)( |_)(success|audit|failure))|information)\s*(\s|\t|,|#\d+|<[^>]+>)\s*(?!(?:[A-Fa-f:\d.]+))[^\t,#<\s.]+\.({domain}[^\s.",]+)""",
      """"(?:winlog\.)?computer_name\\*":\\*"({host}[^\\"]+)""",
      """@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """({event_code}4776)""",
      """The ({login_type_text}computer|domain)(\s\w+)? attempted to validate the credentials""",
      """Logon (?:a|A)ccount(:|=)[\s\\\\t]*(({email_address}[^@\s]+?@[^\s]+?\.[^\s]+?)|(({user}[^@\s,;=\\]+)(?:@({email_domain}[^\s.;,@=]+).*?)?))[\\rnt]*Source Workstation(:|=)([\s\\]+|(\s*\\*((({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)(:({dest_port}\d+))?)|({dest_host}.+?))[\s;]*))Error Code(:|=)""",
      """Error Code(:|=)\s*(\\+t)?({result_code}[\w\-]+)""",
      """Source Workstation(:|=)[\s\\\\t]+((({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)(:({src_port}\d+))?)|({src_host}[^\s]+?))[\s\\\\n\;]*Error Code(:|=)""",
    ],
    DupFields = ["host->dest_nost"]
  

}
```