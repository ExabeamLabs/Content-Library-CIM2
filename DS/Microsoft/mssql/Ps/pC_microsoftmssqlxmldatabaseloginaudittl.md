#### Parser Content
```Java
{
Name = "microsoft-mssql-xml-database-login-audit-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "MSSQL"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<event xmlns="
      "<provider name='mssql"
      "<keyword>audit "
      "<binary>"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<EventID Qualifiers=[^>]+>({event_code}\\d+)"
      "(?i)<Provider Name ='({db_name}[^']+)'"
      "(?i)<Computer>({host}[^<]+)<\\/Computer>"
      "(?i)<Message>({additional_info}[^<]+)"
      "(?i)<Keyword>({result}Audit[^<]+)<\\/Keyword>"
      "(?i)<Message>.+?user\\s'((({domain}[^\\\\']+)\\\\)?({user}[^']+))'"
      "(?i)\\[CLIENT:\\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?"
    ]
    DupFields = [
      "host->dest_host"
    ]
  

}
```