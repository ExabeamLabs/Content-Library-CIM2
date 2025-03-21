#### Parser Content
```Java
{
Name = "phantom-p-kv-email-receive-success-emailreceived"
Vendor = "Phantom"
Product = "Phantom"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
  """from: """
  """,to: """
  """,subject: """
  """,analysed_time: """
  """phantom"""
]
Fields = [
  """,analysed_time:\s*({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)"""
  """from:\s*({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """,to:\s*({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^,]*?)\s*,"""
  """,subject:\s*({email_subject}[^,]*?)\s*,"""
  """,severity:\s*({alert_severity}[^,]*?)\s*,"""
]
SOAR {
  IncidentType = "dlp"
  DupFields = [
    "time->startedDate"
    "vendor->source"
    "rawLog->sourceInfo"
    "email_recipient->dlpUser"
    "email_address->emailFrom"
    "email_subject->emailSubject"
    "email_recipients->emailTo"
  ]
  NameTemplate = "Phantom Phishing Email Alert ${email_subject} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "user"
      Name = "email"
      Fields = [
        "dest_email_address->email"
      ]
    

}
```