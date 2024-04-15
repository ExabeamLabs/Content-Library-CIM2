#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-file-read-success-4663-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<data name"
      "\"eventid\":4663"
      "xmlns"
      "\"activity\":\"4663 - an attempt was made to access an object.\""
    ]
    Fields = [
      "(?i)\"TimeGenerated\"+:\"+({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)\"Computer\"+:\"+({host}[^\"]+)"
      "(?i)\"EventID\"+:({event_code}\\d+)"
      "(?i)<Data Name(\\\\)?=(\\\\)?\"+SubjectUserSid(\\\\)?\"+>(?:NONE_MAPPED|({user_sid}[^<]+))<\\/Data>"
      "(?i)<Data Name(\\\\)?=(\\\\)?\"+SubjectUserName(\\\\)?\"+>(LOCAL SERVICE|({user}[^<]+))<\\/Data>"
      "(?i)<Data Name(\\\\)?=(\\\\)?\"+SubjectDomainName(\\\\)?\"+>(NT AUTHORITY|({domain}[^<]+))<\\/Data>"
      "(?i)<Data Name(\\\\)?=(\\\\)?\"+SubjectLogonId(\\\\)?\"+>({login_id}[^<]+)<\\/Data>"
      "(?i)<Data Name(\\\\)?=(\\\\)?\"+ObjectType(\\\\)?\"+>({file_type}[^<]+)<\\/Data>"
      "(?i)<Data Name(\\\\)?=(\\\\)?\"+ObjectName(\\\\)?\"+>({file_path}({file_dir}.+?)[\\\\\\/]+({file_name}(?:[^<\\\\\\/:]+?)(\\.({file_ext}\\w+))?)|[^\\\\:<]+)<\\/Data>"
      "(?i)<Data Name(\\\\)?=(\\\\)?\"+ProcessName(\\\\)?\"+>({process_path}({process_dir}(?:[^<]+)?[\\\\\\/])?({process_name}[^\\\\\\/\"<]+?))<\\/Data>"
      "(?i)<Data Name(\\\\)?=(\\\\)?\"+AccessList(\\\\)?\"+>({access}.+?)\\s(\\\\t)*"
      "(?i)AccessMask\"+:\"+({access_mask}[^\"]+)"
      "(?i)\"Activity\":\"({event_name}[^\"]+)"

    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```