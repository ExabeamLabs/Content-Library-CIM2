#### Parser Content
```Java
{
Name = "checkpoint-hs-kv-alert-trigger-success-compromizedaccount"
 Vendor = Check Point
 Product = Harmony SaaS
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
 ParserVersion = v1.0.0
 Conditions = [ """"product":"Compromized Account"""", """"product_family":"Email & Collaboration""""]
 Fields  = [
  """"time":"({time}\d{4}-\d{2}-\d{2}T(\d{2}:){2}\d{2})((\+|\-){1,2}\d{1,2}:\d{2})"""
  """"product":"({product_name}[^"]+)""""
  """"action":"({action}[^"]+)""""
  """"appi_name":"({app}[^"]+)""""
  """"account":"({account}[^"]+)""""
  """"severity":"({severity}[^"]+)""""
  """"confidence_level":"({alert_severity}[^"]+)""""
  """"product_family":"({category}[^"]+)""""
  """"verdict":"({result}[^"]+)""""
  """"description":"({additional_info}[^"]+)""""
  """"from_email":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)""""
  """"user":"({full_name}[^"]+)""""
  """"maliciouscontent":"({result_reason}[^"]+)""""
  """"email_subject":"({email_subject}(?:\\.|[^"\\])+)""""
  """"src_user_name":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
  """"src_user_email":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)""""
 ]


}
```