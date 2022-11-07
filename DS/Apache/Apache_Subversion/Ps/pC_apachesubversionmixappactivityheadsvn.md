#### Parser Content
```Java
{
Name = apache-subversion-mix-app-activity-headsvn
Product = "Apache Subversion"
Conditions = [
  """\"HEAD /svn/"""
]
ParserVersion = "v1.0.0"

svn-app-activity = {
  Vendor = Apache
  TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
  Fields = [
    """"Computer":"({host}[\w\-.]+?)""""
    """({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s*[^\s]+\s*(-|({user}[^\s]+))\s*\[({time}\d+\/\w+\/\d+:\d+:\d+:\d+\s*(\-|\+)\d+)\]\s*\\?"({additional_info}({operation}[^"\s]+)\s({object}[^\s"]+).*?)\\?"\s*(?:-|({result}\d+))\s*(?:-|({bytes}\d+))\s+[^\s]+\s+\\?"(-|({user_agent}[^"]+))\\?""""
    """({app}svn)"""

  
}
```