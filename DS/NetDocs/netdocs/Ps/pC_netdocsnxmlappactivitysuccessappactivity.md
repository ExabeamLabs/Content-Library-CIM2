#### Parser Content
```Java
{
Name = "netdocs-n-xml-app-activity-success-appactivity"
Vendor = "NetDocs"
Product = "NetDocs"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """</activity>"""
  """<activity date=""""
  """<user id=""""
  """guid=""""
  """host=""""
  """name=""""
]
Fields = [
  """<activity date="({time}\d\d\d\d-\d+-\d+T\d+:\d+:\d+)" name="(|({operation}[^"]+))" host="(|({host}[^"]+))" desc="(|({=operation}[^"]+))""""
  """<user id="(|({email_address}[^@"]+?@({email_domain}[^"]+))|({user}[\w\.\-]{1,40}\$?))" guid="(|({guid}[^"]+))" name="(|({full_name}[^"]+))""""
]
ParserVersion = "v1.0.0"


}
```