#### Parser Content
```Java
{
Name = "imperva-attackanalytics-cef-alert-trigger-success-attackanalytics"
Vendor = "Imperva"
Product = "Attack Analytics"
TimeFormat = "epoch"
Conditions = [
  """|Imperva Inc|"""
  """|Attack Analytics|"""
  """CloudWAF"""
  """ImpervaAAPlatform"""
]
Fields = [
  """start\\?=({time}\d{13})"""
  """cs7[\\?]+=({alert_name}[^=]+?)\s+\w+[\\?]+="""
  """({alert_type}Attack Analytics)""",
  """Attack Analytics\|([^|]*\|){3}({alert_severity}[^|]+)\|""",
  """src\\?=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """request\\?=(\/|(?i)Distributed|({uri_path}[^\n]+?))\s+requestClientApplication\\?=((?i)Distributed|({app}[^=]+))\s+\w+\\?=""",
  """msg\\?=({additional_info}[^\n]+?)\s+start\\?=""",
  """dhost\\?=((?i)Distributed|({target}[^=]+))\s+\w+\\?="""
  """cs3[\\?]+=({country}[^=]+?)\s+\w+[\\?]+="""
]
ParserVersion = "v1.0.0"


}
```