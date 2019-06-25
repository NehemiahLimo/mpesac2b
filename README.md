[![Open Source Love svg1](https://badges.frapsoft.com/os/v1/open-source.svg?v=103)](https://github.com/ellerbrock/open-source-badges/) [![made-for-VSCode](https://img.shields.io/badge/Made%20for-VSCode-1f425f.svg)](https://code.visualstudio.com/) 
# mpesac2b
MPESA C2B API integration. A demo on MPESA C2B

```
  $url = 'https://sandbox.safaricom.co.ke/mpesa/c2b/v1/simulate';
  $curl = curl_init();
  curl_setopt($curl, CURLOPT_URL, $url);
  curl_setopt($curl, CURLOPT_HTTPHEADER, array('Content-Type:application/json','Authorization:Bearer '.$access_token)); //setting custom header
  $curl_post_data = array(
          //Fill in the request parameters with valid values
         'ShortCode' =>  $shortcode,
         'CommandID' => 'CustomerPayBillOnline',
         'Amount' => '2',
         'Msisdn' => '254725443442',
         'BillRefNumber' => '00000'
  );
  $data_string = json_encode($curl_post_data);
  curl_setopt($curl, CURLOPT_RETURNTRANSFER, true);
  curl_setopt($curl, CURLOPT_POST, true);
  curl_setopt($curl, CURLOPT_POSTFIELDS, $data_string);
  $curl_response = curl_exec($curl);
  print_r($curl_response);
  echo $curl_response;
  ```
