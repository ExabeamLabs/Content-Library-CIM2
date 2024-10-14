#### Parser Content
```Java
{
Name = "trendmicro-ddei-cef-email-receive-success-messagetracking"
Vendor = "Trend Micro"
Product = "Trend Micro Email Security"
TimeFormat = ["MMM dd yyyy HH:mm:ss","MMM dd yyyy HH:mm:ss zZ"]
Conditions = [
  """|Trend Micro|"""
  """|Deep Discovery Email Inspector|"""
  """|MESSAGE_TRACKING|"""
]
Fields = [
  """\s*rt=({time}\w+\s\d+\s\d+\s\d+:\d+:\d+\s\w+[-+]\d+:\d+)"""
  """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\sdvchost=({host}[^\s]+)"""
  """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """duser=({email_address}[^\s]+)"""
  """\scs3=({result}[^\s]+)"""
  """msg=({email_subject}.+?)\scs2"""
  """cs5=({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\s]+)\s"""
  """cs4=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\scs5Label"""
  """\|({alert_severity}\d+)\|rt"""
  """cs1=({return_path}[^\s]+)\s"""
]
DupFields = [
  "email_address->email_user"
]
ParserVersion = "v1.0.0"


}
```