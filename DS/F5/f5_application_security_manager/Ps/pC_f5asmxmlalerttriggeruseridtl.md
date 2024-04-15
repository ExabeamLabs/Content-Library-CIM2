#### Parser Content
```Java
{
Name = "f5-asm-xml-alert-trigger-userid-tl"
    ParserVersion = "v1.0.0"
    Vendor = "F5"
    Product = "F5 Application Security Manager"
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [
      " asm:"
      "https"
      "<userid>"
    ]
    Fields = [
      "(?i)\\w+\\s+\\d+\\s+\\d\\d:\\d\\d:\\d\\d\\s+({host}[^\\s]+)\\s+ASM:"
      "(?i)\\sASM:\"[^\"]*\",\"({time}\\d\\d\\d\\d-\\d\\d-\\d\\d \\d\\d:\\d\\d:\\d\\d)"
      "(?i)\\sASM:(\"[^\"]*\",){2}\"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({dest_port}\\d+))?"
      "(?i)\\sASM:(\"[^\"]*\",){3}\"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?"
      "(?i)\\sASM:(\"[^\"]*\",){4}\"({method}[^\"]+)"
      "(?i)\\sASM:(\"[^\"]*\",){5}\"({protocol}[^\"]+)\""
      "(?i)\\sASM:(\"[^\"]*\",){8}\"({additional_info}[^\"]+)\""
      "(?i)\\sASM:(\"[^\"]*\",){8}\"({alert_name}[^\"]+)\""
      "(?i)\\sASM:\"({alert_name}[^\"]+)\""
      "(?i)\\sASM:(\"[^\"]*\",){9}\"(?:N\\/A|({user}[^\"]+))\""
      "(?i)\\sASM:(\"[^\"]*\",){13}\"\\w+\\s+({malware_url}[^\"]+?)(?:\\s+\\w+\\/\\d\\.\\d|)((\\\\r\\\\n|\\s+)[\\w\\-]+:|\")"
      "(?i)Host:\\s*({domain}[^\"\\\\]+?)(\\\\r|\\\\n|\\s+|\\\\t)"
      "(?i)User-Agent:\\s*({user_agent}[^\"]+?)(\\\\r\\\\n[\\w\\-]+:|\")"
      "(?i)User-Agent:\\s*Mozilla\\/.+?({browser}Chrome|Safari|Opera|(?:F|f)irefox|MSIE|Trident)"
      "(?i)<USERID>({user_id}[^\\\\\\<]+)"
      "(?i)<ACCTID>({account_id}[^\\\\\\<]+)"
      "(?i)<ACCTTYPE>({user_type}[^\\\\\\<]+)"
    ]
    DupFields = [
      "protocol->alert_type"
    ]
  

}
```