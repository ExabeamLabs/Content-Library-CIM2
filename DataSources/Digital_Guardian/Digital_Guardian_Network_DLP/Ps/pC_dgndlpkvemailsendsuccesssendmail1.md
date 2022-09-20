#### Parser Content
```Java
{
Name = dg-ndlp-kv-email-send-success-sendmail-1
  Conditions = [ """Operation="Send Mail"""" , """Server_UTC_Timestamp=""" ]
  ParserVersion = "v1.0.0"

splunk-digitalguardian-dlp-email-out = {
  Vendor = Digital Guardian
  Product = Digital Guardian Network DLP
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Fields = [
    """(Agent_UTC_Time|Server_UTC_Timestamp)="({time}\d+\/\d+\/\d\d\d\d \d+:\d+:\d+ (am|AM|pm|PM))"""",
    """Computer_Name ="([^\/\"]+[\\\/])?({host}[^"]+)"""",
    """User_Name ="(?:|(({email_domain}[^"\/\\]+)[\/\\]+)?({user}[^"]+))"""",
    """Domain_Name ="(?:|({email_domain}[^"]+))"""",
    """Email_Sender="(?:|({email_address}[^"]+))"""",
    """Email_Address="(?:|({email_address}[^"]+))"""",
    """Email_Recipient="([^"]+\-)?({email_recipients}({dest_email_address}[^"@\s;,]+@[^"@\s;,]+[^"]*))"""",
    """Destination_File="(?:|({file_name}[^"]+))"""",
    """Destination_File="(?:|message body|({email_attachment}[^"]+))"""",
    """Destination_File_Extension="(?:|({extension}[^"]+))"""",
    """Email_Subject="(?:|({email_subject}[^"]+?))\s*"""",
    """Bytes_Read="(?:|({bytes}\d+))"""",
    """Operation(_ID)?="({event_code}[^"]+)""""
  ]
  DupFields = [ "email_address->email_user", "dest_email_address->external_address" ]
  SOAR {
    IncidentType = "dlp"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "email_address->dlpUser", "email_address->emailFrom", "email_subject->emailSubject", "email_recipients->emailTo", "file_name->dlpFileName", "bytes->dlpFileSize"]
    NameTemplate = """Digital Guardian DLP Email Alert ${email_subject} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="user", Name ="email", Fields=["email_address->email"]}
    
}
```