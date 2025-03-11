#### Parser Content
```Java
{
Name = bitglass-casb-cef-app-scan-dlpscan
  ParserVersion = v1.0.0
  Conditions = [ """ api.bitglass.com """, """"action":"DLPScan"""" ]

cef-bitglass-system-info}{
  Name = bitglass-casb-cef-app-scan-scantimeout
  ParserVersion = v1.0.0
  Conditions = [ """ api.bitglass.com """, """"action":"ScanTimeout"""" 
}
```