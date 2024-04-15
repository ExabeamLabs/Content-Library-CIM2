#### Parser Content
```Java
{
Name = "microsoft-evpowershell-xml-script-execute-success-4104-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - PowerShell"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<eventid>4104<"
      "microsoft-windows-powershell"
      "scriptblocktext"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d+Z)'"
      "(?i)<Security UserID='({user_sid}[^']+)"
      "(?i)<Computer>({host}[^<]+)<\\/Computer>"
      "(?i)<Data Name ='ScriptBlockId'>({scriptblock_id}[^<]+)</Data>"
      "(?i)Function\\s+'({function}[^']+)"
      "(?i)<Data Name ='MessageTotal'>({message_total}\\d+)"
      "(?i)<Data Name ='MessageNumber'>({message_number}\\d+)"
      "(?i)<Message>({script_message}[^:]+)"
      "(?i)<Data Name ='Path'>({path}[^<]+)</Data>"
      "(?i)<Execution ProcessID='({process_id}\\d+)"
      "(?i)({event_code}4104)"
      "(?i)({event_name}Creating Scriptblock text)"
      "(?i)({process_name}PowerShell)"
      "(?i)\"ScriptBlockText\":\"({scriptblock_text}[^\"]+?)\\s*\""
    ]
    DupFields = [
      "host->src_host"
    ]
  

}
```