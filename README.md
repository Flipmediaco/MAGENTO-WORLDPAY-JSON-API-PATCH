# MAGENTO WORLDPAY JSON API PATCH

By default the Magento 1 Custom Web / Sellxed Worldpay JSON API extension has a camel cased Controller Frontname (WorldpayJsonCw).

WorldPay only supports lowercase Webhook. With some web servers the request URI is case sensative and the lowercase version of the camel cased controller results in a not found error (404).

The patch file converts the frontName from "WorldpayJsonCw" to "worldpayjsoncw". The patch resulst in:-

https://example.com/WorldpayJsonCw/endpoint/index/?c=webhook&a=update

https://example.com/worldpayjsoncw/endpoint/index/?c=webhook&a=update
