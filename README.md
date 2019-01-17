# SmsAero-v2-laravel
SMS Aero for laravel API version 2.

Installation

  Step #1
    composer require cooperav/sms-aero-v2-laravel

  Step #2
    Read the documentation
      https://smsaero.ru/description/api/
    
Usage

Add dependency
  use CooperAV\SmsAero\SmsAero;
  
Send message

        // Create SmsAero instance.
        $oSMSAero = new SmsAero('login','api_key');        
        // We can use it with config file f.e
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
