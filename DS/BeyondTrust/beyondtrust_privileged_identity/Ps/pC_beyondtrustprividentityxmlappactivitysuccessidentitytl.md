#### Parser Content
```Java
{
Name = "beyondtrust-prividentity-xml-app-activity-success-identity-tl"
    Vendor = "BeyondTrust"
    Product = "BeyondTrust Privileged Identity"
    TimeFormat = "yyyy-dd-MM'T'HH:mm:ss"
    Conditions = [
      "seventid=\"event_id_job_account_elevated\""
      "soriginatingapplicationname=\"privileged identity\""
      "<event "
    ]
    Fields = [
      "(?i)\\w{3}\\s\\d\\d\\s\\d\\d:\\d\\d:\\d\\d\\s({host}[^\\s]+)"
      "(?i)dtPostTime=\"({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)sEventID=\"({operation}[^\"]+)"
      "(?i)\\(running as user (({account_domain}[^\\s\\\\]+)\\\\+)?({account}[^\\s\\\\\\)]+)\\)"
      "(?i)\"AccountToElevate\"\\s+value=\"(({domain}[^\\s\\\\]+)\\\\+)?({user}[^\\s\\\\\"]+)"
      "(?i)group '({object}[^\\']+)' on system "
      "(?i)\"TargetSystem\"\\s+value=\"({dest_host}[^\"]+)"
      "(?i)OriginatingApplicationName =\"({app}[^\"]+)"
    ]
    ParserVersion = "v1.0.0"
  

}
```