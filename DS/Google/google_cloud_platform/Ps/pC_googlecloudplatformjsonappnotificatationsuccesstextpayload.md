#### Parser Content
```Java
{
Name = google-cloudplatform-json-app-notificatation-success-textpayload
  Vendor = Google
  Product = Google Cloud Platform
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy-MM-dd'T'HH:mm:ss.SSZ","yyyy-MM-dd'T'HH:mm:ss.SZ" ,"yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"]
  Conditions = [""""textPayload":"""",  """"type":"cloud_run_revision"""",""""revision_name":"""","""dproc=Cloud PubSub"""]
  Fields = [
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)""",
    """"service_name":"({service_name}[^"]+)"""",
    """destinationServiceName =({app}[^=]+?)\s\w+=""",
	  """"region":"({region}[^"]+)"""",
  ]
  ParserVersion = v1.0.0


}
```