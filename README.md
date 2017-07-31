# MiqPay PHP-SDK
Php sdk for [MiqPay ](https://miqpay.ru) 

### Payment integration using MiqPay Api

```php
<?php
header('Content-Type: text/html; charset=UTF-8');

// Miqpay data
$publicKey = '';
$secretKey = '';

// Order params
$params['amount'] = 1;
$params['currency'] = 'RUB';
$params['orderId'] = 1;
$params['paymentType'] = 'app';
$params['payment'] = 'ALL';

require_once('../MiqPay.php');

$miqPay = new MiqPay($publicKey,$secretKey);
$response = $miqPay->api('initPayment', $params);

print_r($response);

if(!empty($response->result->payUrl)){
    header("Location: " . $response->result->payUrl);
}
```

### Direct download

Download [last version ](https://github.com/Miqpay/MIQPAY-PHP-SDK/archive/master.zip) , unzip and copy to your project folder.

## Contributing ##

Please feel free to contribute to this project! Pull requests and feature requests welcome!
