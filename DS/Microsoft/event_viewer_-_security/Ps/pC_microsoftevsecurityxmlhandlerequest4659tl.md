#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-handle-request-4659-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "a handle to an object was requested with intent to delete"
      ">4659<"
      "microsoft-windows-security-auditing"
    ]
    Fields = [
      "(?i)({event_name}A handle to an object was requested with intent to delete)"
      "(?i)({event_code}4659)"
      "(?i)>\\s({host}\\w+)\\s<"
      "(?i)Handle ID:\\s+({object_id}[^\\s]+)\\s+Process Information:"
      "(?i)Transaction ID:\\s+({transaction_id}[^\\s]+)\\s+Accesses:"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d+Z)"
      "(?i)<Computer>({host}[^<>]+)<\\/Computer>"
      "(?i)ThreadID='({thread_id}\\d+)'"
      "(?i)<Keyword>({result}[^<]+)<"
      "(?i)<Task>({operation}File System)"
      "(?i)<Provider>({provider_name}[^<]+)"
      "(?i)Security ID:\\s*({user_sid}\\S+)\\s+"
      "(?i)Account Name:\\s*({user}\\S+)\\s+"
      "(?i)Account Domain:\\s*({domain}\\S+)\\s+"
      "(?i)Logon ID:\\s*({login_id}\\S+)\\s+"
      "(?i)Object Server:\\s*({object_server}\\S.*?)\\s+"
      "(?i)Object Type:\\s*({object_type}\\S+)\\s*"
      "(?i)Object Name:\\s*({object}\\S.+?)\\s+"
      "(?i)Accesses:\\s*(-|({access}[^\\s]+))\\s*"
      "(?i)Process ID:\\s*({process_id}\\S+)\\s+"
    ]
    DupFields = [
      "host->dest_host"
    ]
  

}
```