#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-login-fail-4625-1-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<eventid>4625</eventid>"
      "an account failed to log on"
      "failure reason"
      "computer"
    ]
    Fields = [
      "(?i)({event_name}An account failed to log on)"
      "(?i)TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d.\\d\\d\\d\\d\\d\\d\\d\\d\\dZ)'"
      "(?i)Computer>({host}[^<]+)<\\/Computer"
      "(?i)({event_code}4625)"
      "(?i)Subject(:|=).+?Account Name(:|=)\\s*(-|({src_user}[^\\s@]+?))[\\s;]*Account Domain(:|=)"
      "(?i)Logon Type(:|=)\\s*({login_type}\\d+)\\s+Account\\s"
      "(?i)Account For[\\s;]*Which Logon Failed(:|=)[\\s;]*Security ID(:|=)\\s*(?:\\/?NULL SID|({user_sid}.+?))[\\s;]*Account Name"
      "(?i)Logon Failed(:|=).+?Account Name(:|=)\\s*({user}[^\\s@]+?)[\\s;]*Account Domain(:|=)"
      "(?i)Logon Failed(:|=).+?Account Name(:|=)\\s*({email_address}[^\\s@;]+?@[^\\s@;]+?)[\\s;]*Account Domain(:|=)"
      "(?i)Logon Failed(:|=).+?Account Domain(?::|=)\\s*(|-|({domain}[^\\s]+?))[\\s;]*Failure Information"
      "(?i)Sub Status(:|=)\\s*({result_code}.+?)[\\s;]*Process Information(:|=)"
      "(?i)Workstation Name(:|=)\\s*(-|({src_host_windows}[^\\s;]+))[\\s;]*Source Network Address(:|=)"
      "(?i)Source Network Address(:|=)\\s*[\\\\rnt]*(-|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?)[\\\\rnt\\s;]*Source Port(:|=)"
      "(?i)Logon Process(:|=)\\s*({auth_process}[^\\s;]+)[\\s;]*Authentication Package(:|=)"
      "(?i)Authentication Package(:|=)\\s*({auth_package}.+?)[\\s;]*Transited Services(:|=)"
    ]
    DupFields = [
      "host->dest_host"
      "result_code->failure_code"
    ]
  

}
```