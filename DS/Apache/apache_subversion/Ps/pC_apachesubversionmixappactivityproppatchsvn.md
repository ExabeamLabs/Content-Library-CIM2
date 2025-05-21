#### Parser Content
```Java
{
Name = apache-subversion-mix-app-activity-proppatchsvn
Product = "Apache Subversion"
Conditions = [
  """\"PROPPATCH /svn/"""
]
ParserVersion = "v1.0.0"

svn-app-activity = {
  Vendor = Apache
  TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
  Fields = [
    """"Computer":"({host}[\w\-.]+?)""""
    """({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*[^\s]+\s*(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*\[({time}\d+\/\w+\/\d+:\d+:\d+:\d+\s*(\-|\+)\d+)\]\s*\\?"({additional_info}({operation}[^"\s]+)\s({object}[^\s"]+).*?)\\?"\s*(?:-|({result}\d+))\s*(?:-|({bytes}\d+))\s+[^\s]+\s+\\?("(-|({user_agent}[^"]+))\\?)?("|$)"""
    """({app}svn)"""

  
}
```