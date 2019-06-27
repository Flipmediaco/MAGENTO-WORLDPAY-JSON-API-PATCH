# MAGENTO WORLDPAY JSON API PATCH

By default the Magento 1 Custom Web / Sellxed Worldpay JSON API extension has a camel cased Controller Frontname (WorldpayJsonCw).

WorldPay only supports lowercase Webhook. With some web servers the request URI is case sensative and the lowercase version of the camel cased controller results in a not found error (404).

The patch file converts the frontName from "WorldpayJsonCw" to "worldpayjsoncw". The patch results in...

WEBHOOK URL ORIGNAL:-
https://example.com/WorldpayJsonCw/endpoint/index/?c=webhook&a=update

BECOMING:-
https://example.com/worldpayjsoncw/endpoint/index/?c=webhook&a=update

Once the patch is applied the camel cased Controller Frontname "WorldpayJsonCw" will return 404 and lowercase frontname will be used in all instances.

The patch is recorded to enable the changes to be repeated on upgrade of the original extension.

https://www.sellxed.com/shop/en/eur/magento-worldpay-json-api-zahlungs-extension.html
