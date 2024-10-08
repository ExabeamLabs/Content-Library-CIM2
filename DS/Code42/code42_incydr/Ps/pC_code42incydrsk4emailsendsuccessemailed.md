#### Parser Content
```Java
{
Name = "code42-incydr-sk4-email-send-success-emailed"
Vendor = "Code42"
Product = "Code42 Incydr"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss:SSZ","yyyy-MM-dd'T'HH:mm:ssZ"]
Conditions = [
  """"fileCategoryByExtension""""
  """"eventType":"EMAILED""""
  """"osHostName"""
  """act=send"""
]
Fields = [
  """"eventTimestamp"+:\s*"+({time}\d+-\d+-\d+T\d+:\d+:\d+Z)"""
  """"eventType"+:\s*"+({event_code}[^"]+)"""
  """"source":"+({log_source}[^"]+)""""
  """"eventTimestamp"+:\s*"+({time}[^"]+)""""
  """"fileName"+:\s*"+({file_name}[^"]+?(\.({file_ext}[^\."]+))?)""""
  """"fileCategory"+:\s*"+({file_type}[^"]+)""""
  """"fileSize"+:\s*({bytes}\d+)"""
  """"osHostName"+:\s*"+({dest_host}[^"]+)""""
  """"eventType":"({alert_type}[^"]+)"""
  """"emailSender":"+({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
  """"emailRecipients":\[*"+({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
  """"emailSubject":\[*"+({email_subject}[^"]+)""""
  """"emailRecipients":\[*"+({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
  """"emailRecipients":\[({email_recipeints}[^\]]+)\s*\]"""
]
ParserVersion = "v1.0.0"


}
```