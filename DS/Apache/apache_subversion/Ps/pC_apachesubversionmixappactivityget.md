#### Parser Content
```Java
{
Name = apache-subversion-mix-app-activity-get
  Product = Apache Subversion
  ParserVersion = "v1.0.0"
  Conditions = [ """"GET /svn/""" ]

svn-app-activity = {
  Vendor = Apache
  TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
  Fields = [
    """"Computer":"({host}[\w\-.]+?)""""
    """({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*[^\s]+\s*(-|({user}[^\s]+))\s*\[({time}\d+\/\w+\/\d+:\d+:\d+:\d+\s*(\-|\+)\d+)\]\s*\\?"({additional_info}({operation}[^"\s]+)\s({object}[^\s"]+).*?)\\?"\s*(?:-|({result}\d+))\s*(?:-|({bytes}\d+))\s+[^\s]+\s+\\?"(-|({user_agent}[^"]+))\\?""""
    """({app}svn)"""

  
}
```