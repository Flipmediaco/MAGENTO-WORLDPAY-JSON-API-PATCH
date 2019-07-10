# MAGENTO WORLDPAY JSON API PATCH

By default the Magento 1 Custom Web / Sellxed Worldpay JSON API extension has a camel cased Controller Frontname (WorldpayJsonCw).

WorldPay only supports lowercase Webhooks. With some web servers the request URI is case sensative and the lowercase version of the camel cased controller results in a not found error (404).

The patch file converts the frontName from "WorldpayJsonCw" to "worldpayjsoncw". The patch results in...

WEBHOOK URL ORIGNAL - NOT SUPPORTED BY WORLDPAY:-
https://example.com/WorldpayJsonCw/endpoint/index/?c=webhook&a=update

BECOMING - SUPPORTED BY WORLDPAY:-
https://example.com/worldpayjsoncw/endpoint/index/?c=webhook&a=update

Once the patch is applied the camel cased Controller Frontname "WorldpayJsonCw" will return 404 and lowercase frontname will be used in all instances.

# OneStepCheckout Patch for MAGENTO WORLDPAY JSON API PATCH

Additional patch supplied to resolve multi submission of "proceed to checkout" button. Patch fixes issue created by browser CORS policy, blocking "javascript:void(0);" as action for disabling checkout submission.

The patches are recorded to enable the changes to be repeated on upgrade of the original extension.

# ORIGNAL EXTENSION

https://www.sellxed.com/shop/en/eur/magento-worldpay-json-api-zahlungs-extension.html
