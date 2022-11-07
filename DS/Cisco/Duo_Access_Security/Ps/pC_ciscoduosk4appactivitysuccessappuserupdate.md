#### Parser Content
```Java
{
Name = cisco-duo-sk4-app-activity-success-app-userupdate
  Conditions = [ """"action":"user_update"""", """"event-name":"user-updated"""", """app-username""", """"src-application-name":"DUO"""" ]
  ParserVersion = "v1.0.0"

duo-app-activity-1 = {
  Vendor = Cisco
  Product = Duo Access Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""",
    """"event-name":"({event_name}[^"]+)"""",
    """"action":"({operation}[^"]+)"""",
    """"username":"(({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|({user}[^"]+))"""",
    """"object":"({object}[^"]+)"""",
    """"src-application-name":"({app}[^"]+)"""",
  
}
```