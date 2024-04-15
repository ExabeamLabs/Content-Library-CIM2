#### Parser Content
```Java
{
Name = "microsoft-evterminalservicesgateway-xml-endpoint-login-terminalservice-21-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - TerminalServices-Gateway"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "microsoft-windows-terminalservices-localsessionmanager"
      "<eventid>21<"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime=('+|\"+)({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<EventID>({event_code}\\d+)<"
      "(?i)<Execution ProcessID='({process_id}\\d+)'\\s+ThreadID='({thread_id}\\d+)'"
      "(?i)<Computer>({dest_host}[^<]+)<"
      "(?i)<Security UserID=('+|\"+)({user_sid}[^'\"]+)'"
      "(?i)<User>(({domain}\\S+)\\\\+)?({user}[^<]+)<"
      "(?i)<SessionID>({session_id}\\d+)<"
      "(?i)<Address>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?<"
    ]
    ParserVersion = "v1.0.0"
  

}
```