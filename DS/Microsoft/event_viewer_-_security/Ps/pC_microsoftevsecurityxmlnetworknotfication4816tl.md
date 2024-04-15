#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-network-notfication-4816-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4816<"
      "rpc detected an integrity violation while decrypting an incoming message"
    ]
    Fields = [
      "(?i)<EventID>({event_code}\\d+)"
      "(?i)({event_name}RPC detected an integrity violation while decrypting an incoming message.)"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)"
      "(?i)<Execution ProcessID='({process_id}\\d+)' ThreadID='({thread_id}\\d+)'"
      "(?i)Peer Name:\\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?"
    ]
  

}
```