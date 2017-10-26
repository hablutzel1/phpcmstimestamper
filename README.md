phpcmstimestamper
=================

This PHP project allows to append an RFC 3161 timestamp to an existing CMS signature.

See too https://blobfish.pe/blog/add-rfc-3161-timestamp-to-existing-pkcs-7cms-signature-in-php/.

Basic usage
-----------

Download this Git repository and execute the working sample `demo.php`:

```php
<?php
$originalCmsAsPem = "-----BEGIN CMS-----
MIIFiAYJKoZIhvcNAQcCoIIFeTCCBXUCAQExDTALBglghkgBZQMEAgEwHQYJKoZI
...
1lUaWopfF7uZf5LXZt2Ru5UPr+51ULJRcEeUTA==
-----END CMS-----";
$updatedCms = CmsTimestamper::addTimestampToCms($originalCmsAsPem, "http://tsa.starfieldtech.com");
```