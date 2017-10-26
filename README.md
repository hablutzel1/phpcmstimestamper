phpcmstimestamper
=================

This PHP project allows to append an RFC 3161 timestamp to an existing CMS signature.

Basic usage
-----------

From the demo file `main.php`:

```php
<?php
$originalCmsAsPem = "-----BEGIN CMS-----
MIIFiAYJKoZIhvcNAQcCoIIFeTCCBXUCAQExDTALBglghkgBZQMEAgEwHQYJKoZI
...
1lUaWopfF7uZf5LXZt2Ru5UPr+51ULJRcEeUTA==
-----END CMS-----";
$updatedCms = CmsTimestamper::addTimestampToCms($originalCmsAsPem, "http://tsa.starfieldtech.com");
```