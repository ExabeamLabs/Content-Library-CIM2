#### Parser Content
```Java
{
Name = forcepoint-dlp-cef-email-send-datasecurity
Vendor = "Forcepoint"
Product = "Forcepoint DLP"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """CEF:"""
  """|Websense|Data Security"""
  """sourceServiceName ="""
]
Fields = [
  """\ssuser=({user}.+?)\s+(\w+=|$)"""
  """\sloginName =(({domain}[^\\]+)\\+)?({user}.+?)\s+(\w+=|$)"""
  """sourceServiceName =(SMTP|Endpoint Email).+?suser=([^\\]+\\+)?({email_address}.+?)\s+(\w+=|$)"""
  """sourceServiceName =(SMTP|Endpoint Email).+?loginName =([^\\]+\\+)?({email_address}.+?)\s+(\w+=|$)"""
  """\sduser=\\*(({dest_domain}[^\\]+)\\+)?({target}.+?)\s+fname=.+?sourceServiceName =(?!(SMTP|Endpoint Email))""" 
  """\sduser=({email_recipients}.+?)\s+(\w+=|$).+?sourceServiceName =(SMTP|Endpoint Email)"""
  """\sfname=(N\/A|.*?[\/\\]*({file_name}[^\\\/]+))\s+\- [\d.]+ """
  """\sfname=(N\/A|({email_attachment}.+?))\s+(\w+=|$).+?sourceServiceName =(SMTP|Endpoint Email)"""
  """\sfname=.*\.({extension}[^\s]+)\s+(msg=|- ).+?sourceServiceName =(SMTP|Endpoint Email)"""
  """\smsg=({email_subject}.+?)\s+(\w+=|$).+?sourceServiceName =(SMTP|Endpoint Email)"""
  """\sfname=(N\/A|.*?\.[^\s]+ - ({bytes}[\d.]+)\s+({bytes_unit}[^\s;]+))"""
  """\ssourceServiceName =({alert_type}.+?)\s\w+="""
  """\|Websense\|([^|]+?\|){3}({alert_name}[^|]+)"""
  """\scat=({alert_name}[^;]+).*?\s+sourceService.+?analyzedBy"""
  """\|Websense\|([^|]+?\|){4}({alert_severity}[^|]+)"""
  """\sact=({action}[^\s]*)"""
]
ParserVersion = "v1.0.0"


}
```