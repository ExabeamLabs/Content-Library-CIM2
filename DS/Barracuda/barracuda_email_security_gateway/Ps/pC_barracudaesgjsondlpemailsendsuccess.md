#### Parser Content
```Java
{
Name = barracuda-esg-json-dlp-email-send-success
  ParserVersion = "v1.0.0"
  Conditions = [ """"action":"allowed"""", """"delivered":"delivered"""", """"hdr_from":"""", """"hdr_to":"""", """Queued mail for delivery""" ]
  

barracuda-dlp-email{
	Vendor = Barracuda
    Product = Barracuda Email Security Gateway
    TimeFormat = "yyyy-dd-MM'T'HH:mm:ss"
    Fields = [
      """({time}\d{4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2})Z\s({host}[\w\-.]+)\s"""
      """"action":"({action}[^"]+)""""
      """"src_ip":"({src_ip}[A-Fa-f:\d.]+)""""
      """"delivered":"({result}[^"]+)""""
      """"email":"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
      """"env_from":"({email_address}[^@"]+@[^"]+)"""
      """"subject":"({email_subject}[^"]+?)\s*""""
      """"size":({bytes}\d+),"""
      """"message_id":"({message_id}[^"]+)""""
      """"reason":"({failure_reason}[^"]+)"""
      """"hdr_to":"({email_recipients}(({dest_email_address}[^@,"]+@[^,"]+?),)?[^"]+?)",""",
      """"attachments":\[\{"name":"({email_attachment}[^,"]*(\.({file_ext}[^",]+)))"""

}
```