# DrCrypto
Customer Service 

require _DIR_ . '/vendor/autoload.php';

$bot = new Telegram('1548357825:AAFivBqfBcAtr7aWYa947-jMPJPt1D0HVNc');

$data = $bot->getData();
$chat_id = $data['message']['chat']['id'];
$labeleled = array('label' => 'Example', 'amount' => 30);

$invoice = array(
  'chat_id' => $chat_id,
  'title' => 'Invoice',
  'description' => 'A simple description',
  'payload' => 'test',
  'provider_token' => '284685063:TEST:MmFkM2IwYmYyYzhm',
  'start_parameter' =>'start',
  'currency' => 'GBP' ,
  'prices' => json_encode((array($labeled))));
  
  $bot->sendInvoice($invoice);
