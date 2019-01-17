# SmsAero-v2-laravel
SMS Aero for laravel API version 2.

<h1>Installation</h1>

  <h2>Step #1</h2>
    &emsp;composer require cooperav/sms-aero-v2-laravelL

  <h2>Step #2</h2>
    &emsp;Read the documentation
      &emsp;https://smsaero.ru/description/api/
    
<h1>Usage</h1>

<h3>Add dependency</h3>
  &emsp;use CooperAV\SmsAero\SmsAero;
  
<h3>Send message</h3>

        // Create SmsAero instance.
        $oSMSAero = new SmsAero('login','api_key');        
        // We can use it with config file f.e.
        // config('smsaero.login') and config('smsaero.api_key')
        
        // Set receiver's phone number.
        $phone_number = '111111111';
        
        // Set message content.
        $message = 'SMS Aero';
        
        // Sending channels.
        $type = 'DIRECT'; // In docuimentation describe other types.
        // To send message to another countries need use 'INTERNATIONAL' type.
        
        // Send message.
        $response = $oSMSAero->send($phone_number, $message, $type);
        
        // Default response data -> json. However we can get response in XML format.
