#### Parser Content
```Java
{
Name = "hp-hpilo-str-app-login-success-xmllogin-tl"
    ParserVersion = "v1.0.0"
    Vendor = "HP"
    Product = "HP iLO"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [
      "xml login: "
      "ilo"
    ]
    Fields = [
      "(?i)({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\dZ)"
      "(?i)\\d\\d:\\d\\d:\\d\\dZ\\s({host}[^\\s]+)\\s\\#ILO"
      "(?i)({app}ILO)"
      "(?i)\\slogin:\\s({user}[^\\s]+)"
      "(?i)\\slogin:\\s(\\S+\\s){2}({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?\\(({dest_host}[^\\)]+)\\)"
      "(?i)({event_name}XML login)"
    ]
  

}
```