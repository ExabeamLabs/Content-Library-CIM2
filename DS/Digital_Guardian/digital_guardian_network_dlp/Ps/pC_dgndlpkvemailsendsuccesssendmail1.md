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
    """Computer_Name ="([^\/\\"]+[\/\\]+)?({host}[\w\-.]+)"""",
    """Email_Sender="(?:|({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"""",
    """Email_Address="(?:|({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"""",
    """User_Name ="(?:|(({domain}[^"\/\\]+)[\/\\]+)?({user}[\w\.\-]{1,40}\$?))"""",
    """Domain_Name ="(?:|({domain}[^"]+))"""",
    """Email_Recipient="([^"]+\-)?({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"""",
    """Destination_File="(?:|({file_name}[^"]+))"""",
    """Destination_File="(?:|message body|({email_attachment}[^"]+))"""",
    """Destination_File_Extension="(?:|({extension}[^"]+))"""",
    """Email_Subject="(?:|({email_subject}[^"]+?))\s*"""",
    """Bytes_Read="(?:|({bytes}\d+))"""",
    """Operation(_ID)?="({event_code}[^"]+)""""
  ]
  DupFields = [ "src_email_address->email_user", "dest_email_address->external_address" ]
  SOAR {
    IncidentType = "dlp"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "email_address->dlpUser", "email_address->emailFrom", "email_subject->emailSubject", "email_recipients->emailTo", "file_name->dlpFileName", "bytes->dlpFileSize"]
    NameTemplate = """Digital Guardian DLP Email Alert ${email_subject} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="user", Name ="email", Fields=["email_address->email"]}
    
}
```