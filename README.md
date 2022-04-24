# ci4-url-friendly-encryption
A custom library to that allow Codeigniter 4 encryption and decryption result to be pass on url.  

## How to use?
Download the ci4-url-friendly-encryption library and put in your project app/Libraries

## Usage
You can use the library on any Controller, here is the example:

```php
<?php
namespace App\Controllers;
use App\Libraries\Secure; //include the library here

class YourController extends BaseController
{

  public function __construct(){
    $this->secure = new Secure(); //initialize the library onto constructor.
  }
  
  public function encryptstring($string){
    $cipher = $this->secure->enc($string);
    echo $cipher;
  }
  
  public function decryptcipher($cipher){
    $string = $this->secure->dec($cipher);
    echo $string;
  }

}
```
## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[APACHE 2.0](apache-2.0)
